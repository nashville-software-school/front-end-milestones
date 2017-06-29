# Blog Part 3

## Prerequisites

> :warning: This exercise requires that you have completed the [Blog Part 2](../../2-single-page-applications/exercises/SP_JS_XHR_BLOG_02.md) exercise.

## Setup

1. Create a branch in your `blog` repository named `version-3`, and switch to that branch. `git checkout -b version-3` will create and switch you into that branch.

> This project is made up of several parts. By creating a branch for each section you will be able to preserve the concepts you have learned and able to reference them in the future. We have mentioned you should be commenting your code, right?

## Requirements

Time to modularize your blog and access your posts from Firebase. At this point you should have a minimum of 5 personal blog posts.

### Part One

1. Install Grunt to at least watch and lint your javascript files.
1. Refactor your code to utilize the jQuery library.

### Part Two

1. Create two modules
    - blog_controller.js
    - blog_factory.js
1. The blog_controller module should contain all of the DOM interaction.
1. The blog_factory should contain only calls to Firebase.
1. Upload the json file you created for the Blog 2 exercise to Firebase.
1. When the index page loads, get the posts from Firebase via ajax using promises.