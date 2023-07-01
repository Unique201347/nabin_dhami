---
title: Third post
description: thiredfhfhj  dfhbdfb fhd post.
date: '2023-4-14'
categories:
  - sveltekit
  - svelte
published: true
---

## Table of Contents

## Introduction

You learned JavaScript. Maybe you watched a course. You felt confident in your abilities. The voice is gone. There's silence. You open your editor with a blank stare. You feel lost. What now?

[Source code](https://github.com/joysofcode/vanilla-todo) on GitHub.

## Disillusion

Have you watched a cooking show? The chef makes it look easy. Behind the scenes there's a lot of people responsible for that. Someone needs to scrub the pans, taste test, and style the food before they present it to you. Tutorials are like a cooking show where they can set unrealistic expectations, and make you feel like you don't get it. They give you the false impression the person knows everything. You'll be relieved to know — they don't! They're just great cooks.

Don't compare yourself with the experience of someone else. It takes time and practice.

> _“Talent is a pursued interest. Anything that you're willing to practice, you can do.”_ ― Bob Ross

You might have heard well intentioned things such as _"just go work on projects"_. It's easier said than done. Where do you start?

These are tools, and techniques for your mind to reason about code. I want to give you confidence. Instead of feeling stuck and frustrated, you're going to get excited about learning.


You might have heard well intentioned things such as _"just go work on projects"_. It's easier said than done. Where do you start?

These are tools, and techniques for your mind to reason about code. I want to give you confidence. Instead of feeling stuck and frustrated, you're going to get excited about learning.

## The Project

I like the idea behind the [TodoMVC](http://todomvc.com/) project. We're going to create a similar todo app. The styles are going to be simple. They're included in the [source code](https://github.com/joysofcode/vanilla-todo), so we can focus on what's important.

## Breaking Down Problems

I want you to think for a second. How would you build something like this? The answer may be different based on your experience. We often look at things like they're a black box. _"I don't understand it, so I shouldn't bother"_. Everything is just a sum of it parts. We can break it down into managable pieces.

A todo app is a simple create, read, update, delete ([CRUD](https://en.wikipedia.org/wiki/Create,_read,_update_and_delete)) application. It's the basis of everything. Think of huge sites like Reddit, Instagram, Facebook, or Twitter. It's just a CRUD app with extra sauce.

A todo app has all the right fundamentals. Regardless of language, or framework you're learning. It's a great barometer that shows you how it works.

Your first impulse might be opening your editor and starting to code something up. That's a frequent mistake. Step back for a moment and think of the requirements.

## Requirements

- Input field for the todo
- Displaying the todos
- Create todo
- Update todo
- Delete todo

That's it! Nothing crazy. Notice how we're missing the _read_ part of CRUD. We're just going to use an object to keep it simple. We can treat it as our database.


```
function updateUI() {
  inputEl.value = ''

  const todosHTML = `
    <ul>
      ${todos
        .map(({ id, todo }) => {
          return `
            <li class="todo" data-todo="${id}">
              <input class="todo-checkbox" type="checkbox">
              <label class="todo-label" data-todo-label>${todo}</label>

              <input class="todo-update" style="display: none" data-update-input />
              <button class="todo-update-toggle" data-update-btn>✏️</button>
            </li>
          `
        })
        .join(' ')}
    </ul>
  `

  todoListEl.innerHTML = todosHTML
}
```
