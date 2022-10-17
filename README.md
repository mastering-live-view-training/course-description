# Mastering LiveView Training

## Course Description 

LiveView empowers developers and teams to be highly productive by keeping your brain firmly focused on the server-side. Backed by OTP, it brings a fast and fault-tolerant UI to your web apps and enables you to build complex interactive and real-time features easily. In this training, you’ll master the tools you need to be a productive LiveView developer.

Over the course of this six hour training, you’ll build out a real LiveView application and learn how LiveView works under the hood to support interactive UIs, how to build basic forms, how to make your forms more advanced with live uploads, how to secure your LiveViews with live sessions and LifeView lifecycle hooks, how to design layered UIs with components, how to test your LiveViews, how to support advanced client-side interactions with the JS commands API, and how to integrate PubSub into your live views for real-time functionality.

You’ll get hands-on experience by pairing up with your classmates to iteratively build out a set of features into a real LiveView app, interspersed with brief lectures and code samples from your instructor. This workshop will provide the absolute novice with everything you need to develop LiveView professionally, and it will help the more experienced LiveView developer gain deeper insight into LiveView under the hood and LiveView best practices.

Workshop participants will receive and retain full access to the lecture slide decks and project code with instructions and solutions.

## Workshop Structure

We'll balance brief lectures to introduce new concepts with hands-on sessions in which you'll iteratively build out the features that make up our app. You'll be given access to a GitHub repo that contains our app, and each lesson will correspond to a given branch. That branch will hold the starting state of the code for that lesson, and you'll use that branch to build out the feature for that lesson.

Because this workshop optimizes for a hands-on learning approach, you'll split up into pairs in a breakout Zoom room to complete the coding portion of each lesson. This will enable you to collaborate with and learn from each other, and it helps ensure that your instructor can visit each breakout session pair to check in and answer questions in a small setting.

## Prerequisites

You'll need:

* Elixir installed on your machine
* The latest version of Phoenix installed on your machine
* Postgres server up and running on your machine

On the day of the workshop, I'll provision access to the lecture slide decks and the GitHub repo that contains the project we'll be working on.

## Materials
* [GitHub repo](https://github.com/mastering-live-view-training/live-library/tree/main) - You'll get access to this on the day of the training and your acecss will not expire.
* [Lecture slide decks](TBD) - You'll get access to this on the day of the training and your acecss will not expire.

## Completing The Coding Portions

First, **fork** the repo linked above. Then, to complete the coding portion of each lesson, you'll checkout a branch `lesson-<num>` to get the starting state of the code for the given lesson. When you're done (or for guidance during the coding portion of the given lesson), you can view the completed code at the `lesson-<num>-end` branch.

For example, after the lecture portion of lesson 1, you'll checkout `lesson-1` branch to get started coding. When you're done, you can view the completed code for that lesson at `lesson-1-end`. And so on for each of lessons 1-9.

## Course Outline

  - [1. Introducing LiveView: The Book Index Live View](#1-introducing-liveview-the-book-index-live-view)
  - [2. Basic LiveView Components: The Book Show Live View](#2-basic-liveview-components-the-book-show-live-view)
  - [3. Basic Forms: Admin Live Views and Book Forms](#3-basic-forms-admin-live-views-and-book-forms)
  - [4. Testing LiveView: Book Index Unit and Integration Tests](#4-testing-liveview-book-index-unit-and-integration-tests)
  - [5. LiveView Auth: The Admin Live Session](#5-liveview-auth-the-admin-live-session)
  - [6. Advanced Re-Usable Components: The Book Review Component](#6-advanced-re-usable-components-the-book-review-component)
  - [7. Bonus: JavaScript Commands: Toggling the Book Search Form](#7-javascript-commands-toggling-the-book-search-form) - Bonus content will be reviwed time permitting. Any content we don't have time to dive into will still be available to you via lecture slide decks and completed assignment solutions.
  - [8. Bonus: LiveView and PubSub: Build a Real-Time "Checked Out Books" Tracker](#8-liveview-and-pubsub-build-a-real-time-checked-out-books-tracker) - Bonus content will be reviwed time permitting. Any content we don't have time to dive into will still be available to you via lecture slide decks and completed assignment solutions.
  - [9. Bonus: Advanced Forms: File Uploads for Book Covers](#9-advanced-forms-file-uploads-for-book-covers) -  Bonus content will be reviwed time permitting. Any content we don't have time to dive into will still be available to you via lecture slide decks and completed assignment solutions.

## 1. Introducing LiveView: The Book Index Live View

In this first lesson, we'll cover LiveView basics including:

* Basic Routing
* The LiveView lifecycle
* Responding to user events

You'll build a simple live view for the books index page and give the user the ability to checkout and return a book.

## 2. Basic LiveView Components: The Book Show Live View

We'll cover:

* Routing between Live Views
* Using Live Components to wrap up behavior
* Use Function Components to wrap up markup

You'll build the book show live view and add a link to that page from the index. Then, you'll refactor the "checkout/return" book code into its own set of live and function components and call it from the books index page.

Stretch goal: Add the checkout component to the book show page too, so that a user can also checkout a book from that page as well as the index.

## 3. Basic Forms: Admin Live Views and Book Forms

In this section, we'll introduce some admin routes and live views and give admin users the ability to create or edit a book.

We'll cover:

* Advanced routing with the help of live actions
* Basic form functionality with components

You'll build a admin books index and show page, and a dedicated book form component.

## 4. Testing LiveView: Book Index Unit and Integration Tests

In this section, we'll introduce LiveView testing best practices and write some live view tests.

We'll cover:

* LiveView unit tests
* LiveView integration tests
* Tips for testing message passing
* Tips for testing components

We'll build some tests for the books index page and the checkout book functionality.

## 5. LiveView Auth: The Admin Live Session

In this section, we'll discuss the authentication and authorization needs of your live views.

We'll cover:

* Why you need to authenticate live views in the router _and_ when they mount
* How to use shared live sessions and live view callbacks to do so neatly

You build a shared live session to contain your admin routes and a shared module for authenticating and authorizing those routes.

## 6. Advanced Re-Usable Components: The Book Review Component

In this section, we'll build a highly dynamic and re-usable function component.

We'll cover:

* Component slots
* Yielding variables up from component slots to the caller

You'll build a reusable Bootstrap-inspired card component and use it to dynamically render book reviews on the book show page.

## 7. JavaScript Commands: Toggling the Book Search Form

In this section, we'll use JS commands (also called "JS bindings") to implement some simple but common UI interactions in LiveView, entirely on the client side, without writing JavaScript.

We'll cover:

* Composing layered UIs with components
* Introducing the JS commands functionality
* Using JS commands to toggle some markup

You'll build a live component to contain a book search form, and a function component to render a search icon. Then, you'll use JS commands to toggle that search form when the user clicks the search icon.

## 8. LiveView and PubSub: Build a Real-Time "Checked Out Books" Tracker

In this section, we'll leverage PubSub to bring distributed real-time functionality to our LiveView app.

We'll cover:

* Integrating PubSub into your Live View
* Responding to PubSub events on the server by updating what's rendered by the client

You'll build real-time functionality into the app such that, when a user anywhere in the world checks out or returns a book, all users viewing the books index page will see the book's "checkout/return" button update accordingly to reflect the new state of the book.

## 9. Advanced Forms: File Uploads for Book Covers

We'll cover the LiveView File Upload API and how to:

* Upload files
* Render upload progress
* Render upload errors
* Render image previews

You'll build file upload functionality into your book form so that the admin user can upload a book cover image.

