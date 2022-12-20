---
title: Questions to answer for all content
---

## Questions to answer for all content

This page provides guidelines on writing documentation and questions that **every page of content** needs to answer.

The questions are:

* Who
* What
* When
* Where
* Why

Only after you’ve answered these questions, can you explain:
* How

## Who

* Who is the content for? (e.g., the audience)
* Who is the content not intended for?

## What

* What is the purpose of the content?
* What is being documented? (e.g., a product, service, UI feature, functionality, etc)
* What assumptions are you making? (e.g., about the user’s skill-levels, what they know, etc)
* What dependencies exist for whatever is being discussed? (e.g., does the system need to be setup a certain way, what's the minimum viable setup, database before tables before data, etc)
* What is the actual order of events? (e.g., should the user have already performed/installed/completed something else before starting)
* What state should the system/application/source or target machine be in before performing any activities?

## When

* When should the user be aware of different things? (e.g., is there an order of events)
* When is it appropriate to perform what is being discussed (e.g., certain conditions, certain dependencies in place; is it a workaround to an issue, etc)
* When is it not appropriate to perform what’s being discussed (e.g., Product 1 functionality not the same as Product 2, etc)

## Where

* Where are things going to take place? (e.g., Product 1 vs Product 2, specific UI, API vs CLI, Database 1 vs Database 2, etc)
* Where should this not be performed (e.g., Product 1 vs Product 2 again; Functionality that only accepts certain inputs, etc)
* Where can the user pause in the process? (e.g., are there points they can stop and come back? If so, are there logical breaks you can add in?)
* Where does the user perform different actions (e.g., their database, JSON files, CLI, API, Product 1 or Product 2 UI, etc) and is there sufficient information to guide them to these?

## Why

* Why is the user here?
* Why this method and not another?
* Why do this at all?
* Why a certain syntax, structure or other method of presenting data?

## How

This answer depends on answering the previous questions, and should not be written first.

* How does the user perform the task
* How should the system be setup before commencing the task?
* How does the system work once they’ve performed said task?
* How many changes of context are there in the sequence of steps (e.g., A set of UI pages, API vs UI, Source database vs CLI vs FeatureBase database)
* How should tasks be performed? (e.g., in what order)
