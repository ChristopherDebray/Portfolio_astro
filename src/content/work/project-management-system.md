---
title: Project management system
publishDate: 2024-05-22 00:00:00
status: in progress
img: /assets/works/task_management.png
img_alt: Task management system
description: |
  A task management system inspired by JIRA.
  The focus here was to learn Laravel and to focus it's specificities and optmisiations.
  (I used Laravel 10 at first and upgraed to 11 after it came out)
link: ''
tags:
  - Laravel
  - Blade
  - AlpineJS
technos:
  - Reverb
  - Echo
  - Breeze
  - Phpstan
  - Phpunit
  - Pest
  - Tailwind
  - Vite
  - Docker
  - Laravel Blueprint
  - GitlabCI
---

## Laravel the magic one.

> I wanted to re focus on back-end frameworks and dig deeper into it.

Before this project, I was working more on the front-end on my personal project, trying to learn <strong>React</strong> for my Pokedex project.

In my past experience, I used <strong>Symfony</strong>, another PHP framework. Initially, we worked with Symfony 4.4 on a monolithic project, utilizing <strong>JQuery</strong>, <strong>Bootstrap</strong>, and <strong>Webpack</strong>. Later, we embarked on a new project using Symfony 6.1, incorporating functional testing with PHPUnit, usage of <strong>API Platform</strong>, and more.

Althought it was very interesting, I was always curious about <strong>Laravel</strong>.
A friend of mine told me about it's "magic", the multiple commands that you are able to use allowing to create many classes, seeders and such, but also some very specific libraries such as Laravel Blueprint.

### Why this project ?

I had spent a lot of time recently using front-end framework, first <strong>VueJS</strong> (at work but also on my free time), but also <strong>React</strong>.
On react i learned a lot about <strong>Storybook</strong>, <strong>Emotion</strong> with styled component and component testing (<strong>Jest</strong>).
It also allowed me to implement my first CI/CD (with gitlab CI) deployed on a digital ocean server with a linux environemt.

So my goal here was to refocus a bit on the back-end side, i had a lot of ideas, but a clone of JIRA allowed me to think of multiple aspects of a web project.

### What aspects of interest ?

- <span class="title">Environment setup</span> : Not specific to this project, but i like to have a proper setup, with a good docker image and docker compose usable by anyone (also usefull for <strong>CI/CD</strong>), also a <strong>makefile</strong> to store the most frequently used scripts.
- <span class="title">Complex role management</span> : with roles varying on the organisation or project he is a part of (a user can be an editor inside a project while being only a viewer for a specific project etc).
- <span class="title">Conceptual data model</span> : I needed to think my whole database carefully, with it's role complexity, it's relations (user can be linked to many tables) it could quickly become badly optimized.
- <span class="title">Refactoring</span> : I do refacator at "Club employés" but here it was also about putting willingly some "plot holes" here and there, knowing I would have to refactor later, mixing the long term vision on some part (database with blueprint) and a shorter vision with refactoring. Adaptation and having a long term thinking being very important for a good developer.
- <span class="title">Optimisation</span> : Plan, Prepare, Produce, Perfect. After succeding on an implementation and while i am doing it i try to search for any optimisation that could be used, for exemple
"I eager load this and use cache okay, but can't i also optimize this request ? Couldn't i put this information directly in X table to avoid unnecessary joins ?" and such.

### Features

This project is a task management system inspired by JIRA, in it you can create your own organisation, on thoose you will be able to add projects, for organisation and projects you are able to invite users to join with mutliple roles.
And of course, create tasks, with custom statuses, assignee and priority.

- Create and handle your organisation and projects.
- Configurate your organisation and project, with user invitations, custom task prefix, etc.
- Advanced filtering for task listing.
- Create your tasks.
- <span class="inProgress hasAfterIcon has-tooltip">Create custom statuses. <span class="tooltip">in progress</span> </span>
### Libraries / technologies used
