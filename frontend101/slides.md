---
# try also 'default' to start simple
theme: default
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# font
fonts:
  # basically the text
  sans: 'Roboto'
  # use with `font-serif` css class from windicss
  serif: 'Roboto Slab'
  # for code blocks, inline code, etc.
  mono: 'Fira Code'
# some information about the slides, markdown enabled
info: |
  ## Frontend 101
  Get started with JavaScript ES6 and React

  by [Marcus Lee](https://github.com/marcustut)
---

# Frontend 101

Introduction to Frontend Development with JavaScript ES6 and React

<div class="abs-tr !mx-6 !my-8 flex flex-col">
  <img src="https://i.ibb.co/tBrgG4n/Yabee-Cart-BG.png" class="w-12 m-auto rounded-lg">
</div>

<div class="abs-bl !mx-14 my-12 flex flex-col">
  <div class="mb-3 uppercase tracking-widest font-medium">
  Marcus Lee
  </div>
  <div class="text-md opacity-50">Tech Lead, LS Smart Machinery</div>
</div>

<style>
div {
  @apply text-left font-sans;
}
p {
  @apply text-xl;
}
</style>


<!--
-->

---
layout: intro
---

# Marcus Lee

<div class="leading-8 opacity-80">
Tech Lead at LS Smart Machinery<br>
Do full-stack development with React and Go<br>
Love and contribute to open-source<br>
</div>

<div class="my-10 grid grid-cols-[40px,1fr] w-max gap-y-4">
  <ri-github-line class="opacity-50"/>
  <div><a href="https://github.com/marcustut" target="_blank">marcustut</a></div>
  <ri-instagram-line class="opacity-50"/>
  <div><a href="https://twitter.com/geminimarcus" target="_blank">geminimarcus</a></div>
  <ri:linkedin-box-line class="opacity-50"/>
  <div><a href="https://www.linkedin.com/in/geminimarcus/" target="_blank">Marcus Lee</a></div>
</div>

<img src="https://i.ibb.co/yXk05kt/Kai-Yang-Pic1-compressed.jpg" class="rounded-full w-40 h-40 object-cover abs-tr mt-16 mr-12"/>

<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/guide/syntax#embedded-styles
-->

<style>
</style>

---
layout: center
---

# Table of Contents

<ul>
  <li>
    <div class="flex items-center font-medium text-indigo-500">
      1. JavaScript and ES6 <logos:javascript class="ml-2" />
    </div>
  </li>
  <li>
    <div class="flex items-center font-medium text-blue-500">
      2. TypeScript <vscode-icons:file-type-typescript-official class="ml-2" />
    </div>
  </li>
  <li>
    <div class="flex items-center font-medium text-blue-400">
      3. React <logos:react class="ml-2" />
    </div>
  </li>
</ul>

<style>
ul {
  list-style-type: none;
}
</style>

---

# What is frontend?

Frontend is basically what you see and what you interact with!

<div class="flex items-start">

<Tweet id="1402320383932502021" />
<Counter :count="10" class="ml-3 mt-3" />

</div>

<style>
.footnotes-sep {
  @apply mt-20 opacity-10;
}
.footnotes {
  @apply text-sm opacity-75;
}
.footnote-backref {
  display: none;
}
</style>

<!-- Basically frontend is whatever you see and whatever you interact with, be it a button,
a gesture, or whatever UI components it is. Frontend is also not limited to just a webpage,
a mobile app can also be a frontend, or even an old terminal eg. LRT station.
-->

---

# Frontend vs Backend

Let's see some code examples 

<div class="grid grid-cols-2 gap-x-4">

```html 
<div>
  Login to continue
  <button onclick="login()">Login</button>
</div>

<script>
  function login() {
    // do something
  }
</script>

<style>
  div {
    width: '100%';
  }
</style>
```

```ts 
const express = require('express')
const app = express()
const port = 3000

app.get('/users/:userId/books/:bookId', function (req, res) {
  const result = db.fetch('...')
  res.send(result)
})
```
</div>

<!-- 
Let's see some code and compare frontend and backend.

One thing to note here: Frontend refers to Client-side rendering (your code runs at the client)
whereas backend refers to server-side (runs at a server)
-->

---
layout: center
class: text-center
---

# JavaScript and ES6

What is [ES6](https://www.w3schools.com/js/js_es6.asp) and why do we need it?

---
preload: false
---

# JavaScript and ES6

JavaScript is a very messy language due to its nature, ES6 was created to
standardize it. ES6 stands for ECMAScript 6. Basically, we want to achieve <Write Less, Do More>

<div class="grid grid-cols-2 gap-x-4">

```js
// 1. Variables
var a = 5; // the old way
let b = 5; // introduced in ES6
const c = 5; // introduced in ES6

// `var` is global-scoped
// `let`, `const` is block-scoped
```

```js
// 2. Data parsing
const arr = [3, 123, 1023, 23, 5, 78]

// the normal way
let filtered = [];

for (let i = 0; i < arr.length; i++) {
  if (arr[i] > 100) {
    filtered.push(arr[i]);
  }
}

// the ES6 way
let filtered = arr.filter((x) => x > 100);
```

</div>

<!--
I won't go too details about ES6, there are much more about it you can find online
  I'll go through the biggest change and particularly focusing on 'Data parsing'
  This is important because we need ES6 to start exploring on React
-->

---
layout: center
class: text-center
---

# Live Coding!

[Click me to enter CodeSandbox 💻](https://codesandbox.io/s/frontend101-9vyj6)
