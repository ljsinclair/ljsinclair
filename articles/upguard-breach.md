---
title: "Stealing the crown jewels"
date: 2019-08-08

---

**Update** - within days of writing this article, <a href="https://www.theguardian.com/technology/2019/aug/14/major-breach-found-in-biometrics-system-used-by-banks-uk-police-and-defence-firms" target="\_blank" rel="noopener">an almost identical breach occurred in the United Kingdom</a>
{: .notice--info}

On July 1st this year, <a href="https://www.upguard.com/breaches/data-leak-neoclinical-australia-new-zealand" target="\_blank" rel="noopener">Upguard.com</a>, a US based cyber-security company detected and reported a publicly accessible MongoDB database with the name “neoclinical”.

<a href="https://www.linkedin.com/company/neoclinical" target="\_blank" rel="noopener">Neoclinical</a> happens to be an Australian based company that helps match patients with active clinical trials through collection of personal and medical data.

<!--more-->

<a href="https://www.zdnet.com/article/upguard-finds-information-on-over-37000-australia-and-new-zealand-clinical-trial-participants-in-the-wild" target="\_blank" rel="noopener">According to reports</a>, Upguard were able to breach the MongoDB database through hacking a user account, a simple username and password combination. This formed a single point of failure which exposed 37,000 patient records, together with entities responsible for connecting patients with trials, questions used to match patients, and user accounts of the medical organizations administering the trials.

> If it's on the internet, it's a target.

Luckily for Neoclinical, Upguard did their best to help; the security researcher contacted the company through their official telephone numbers and email addresses, monitored the situation then escalated to Amazon Web Services Security when the database remained online. AWS took down the database within 24 hours. However, what's not clear, and may never be, is how long the database was publicly accessible, and whether it had already been hacked.

## What went wrong?

There's two main questions to answer;

First, why was the database exposed to the internet, even if <a href="https://www.theage.com.au/business/companies/thousands-of-medical-histories-exposed-in-data-breach-20190807-p52euq.html" target="\_blank" rel="noopener">it was password protected</a> as Neoclinical's spokesperson stated?

There are two possibilities, either a configuration issue, where the database was mistakenly made publicly accessible, or perhaps this was by design, so different parties could access the data via web forms, direct access or via apps.

> ...with a Zero Trust approach, nothing is trusted and everything is verified in every interaction.

Nonetheless, naming the database "neoclinical" automatically linked it to the company, which undoubtedly made it a more tempting target.

Second, the user account breached by Upguard had access to the entire database, data and user accounts. This was a deliberately created user account, because unlike other databases, MongoDB has no default SuperUser account. Regardless, there was such an account at the time of the breach. With this level of access, Upguard could have created multiple login accounts then started exfiltrating data. Administrator accounts are a necessary evil, but there are ways to restrict access to both data and administrative functions which should be used. The problem lies in those situations where they are not.

## How could this have been avoided?

The Neoclinical breach proves one thing categorically: making a database publicly visible is a mistake. If it's on the internet, it's a target. This scenario is the equivalent to putting the British Crown Jewels in a glass box out front of Buckingham Palace guarded by a single, if heavily armed, Queen's Guard Infantryman. If you can get past the guard, the jewels are yours for the taking.

Another reason for making a database publicly accessible is to act as a honeypot for hackers. The issue lies in the unintentional exposure.

So, securing the database is the first order of business. This can be done through database permissions,  perimeter security, firewalls, and suchlike that protect the database. Then you can add VPNs (Virtual Private Networks) or SSH (Secure SHell) to secure the network.

However, these are are no guarantee of security. For example, <a href="https://www.wired.com/story/equifax-breach-no-excuse/?verso=true" target="\_blank" rel="noopener">Equifax</a> was breached due to unpatched hardware. So the next level of protection should include a Zero-Trust approach to database access.

*"Zero Trust"* begins with the assumption that your network has already been breached; the barbarians aren't at the gates, they're on both sides of them! So with a Zero Trust approach, nothing is trusted and everything is verified in every interaction. Neoclinical's MongoDB database is a case in point; it was on the internet, **secured with a weak password!**

So how do you determine who should have access? In Neoclinical's case, these users can be broken down into four categories:

* An administrator account to configure and administer the database itself, but who is unlikely to require access to the data.

* The patients who fill out the web forms, who add their data, and according to legislation such as GDPR and Australia's on Privacy laws, must be owners of the data, have free access to it, and determine who or what has access.

* The third parties performing analyses on patient data and trial requirements, but not patient identification.

* The trial administrators themselves who contact or are contacted by successful patients.

The problem now is how users get past the firewall and countermeasures and onto whatever secure network you've erected. Make it too hard and users will just give up. Make it too easy, and you get breached.

This conundrum can be solved by adding a new level, a tool that can manage database access, configured to handle the network, the firewall and countermeasures. Then, you add user accounts, hardened with additional security. Lastly, you configure these accounts to access only the data relevant to their role.

This application needs to apply zero-trust principles regarding database access, which can be broken down as follows:

* Secure all direct database credentials (such as the logins to the database the Upguard researcher used)

* Manage all secure database connections.

* Allow creation of user accounts, including additional authentication methods such as two-factor and push authentication.

* Control user account access to data; users see only what they're authorized to view, edit or delete.

* Allow connection only for authorized users.

* Notify and log connection attempts for audit and administration purposes.

## What does this mean in context?

Neoclinical implemented a publicly accessible login to their database. The researcher was able to breach the database and access the entire system using a username and password combination.

## How can this be avoided? ##

Securing the database is the first step, but there's a balancing act between security and access. Users and applications still need to connect to do their work. Make security too tight, and you prevent the work.

<a href="https://mamori.io" target="\_blank" rel="noopener">Mamori.io</a> is an all-in-one tool that simplifies this process in one application, and its deployment would have avoided the Upguard scenario in these ways:

* Databases are not public facing and can be securely firewalled; they're only accessible to the Mamori application.

* Database access is controlled through login to Mamori, and added authentication including multifactor and push authentication used on user devices to confirm legitimate login attempts.

* Access Policies are used to control who can login, when they can login, their location, even their IP.

* Database Policies add Masking, Encryption and Hashing to data on a user or role basis.

* Roles govern the Database privileges and the tables an account can query.

## In summmary ##

At a fundamental level, public facing databases are inherently dangerous. Every business and DBA has to manage ease of use with securing their data. This can be performed through complex server and database configuration with a number of tools. And it can break for the smallest reason. Hackers can target unpatched hardware, poorly configured software and even the humans that use them.

Mamori takes these elements out of the equation. You can secure your systems completely, while making access to the data simple.

## Sources ##

* <a href="https://www.upguard.com/breaches/data-leak-neoclinical-australia-new-zealand" target="\_blank" rel="noopener">Upguard.com neoclinical breach analysis</a>

* <a href="https://www.theage.com.au/business/companies/thousands-of-medical-histories-exposed-in-data-breach-20190807-p52euq.html" target="\_blank" rel="noopener">The Age newspaper article on the breach</a>

* <a href="https://www.linkedin.com/company/neoclinical" target="\_blank" rel="noopener">Neoclinical Linkedin Profile</a> - At time of writing, the neoclinical website is down, likely due to the breach.

* <a href="https://www.zdnet.com/article/upguard-finds-information-on-over-37000-australia-and-new-zealand-clinical-trial-participants-in-the-wild/" target="\_blank" rel="noopener">Zdnet report on the breach</a>

* <a href="https://www.wired.com/story/equifax-breach-no-excuse/?verso=true" target="\_blank" rel="noopener">WIRED report on Equifax</a>

* <a href="https://www.theguardian.com/technology/2019/aug/14/major-breach-found-in-biometrics-system-used-by-banks-uk-police-and-defence-firms" target="\_blank" rel="noopener">Guardian Australia report on UK database breach</a>
