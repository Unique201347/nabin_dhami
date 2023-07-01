---
title: Second
description: Second post.
date: '2023-4-16'
categories:
  - sveltekit
  - svelte
published: true
---

## Svelte

Media inside the **static** folder is served from `/`.

```js
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
