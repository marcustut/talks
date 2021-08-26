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
  sans: "Roboto"
  # use with `font-serif` css class from windicss
  serif: "Roboto Slab"
  # for code blocks, inline code, etc.
  mono: "Fira Code"
# some information about the slides, markdown enabled
info: |
  ## Backend 101
  Get started with Go and PostgreSQL

  by [Marcus Lee](https://github.com/marcustut)
---

# Backend 101

Introduction to Backend Development with Go and PostgreSQL

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

<style>
</style>

---
layout: center
---

# Table of Contents

<ul>
  <li>
    <div class="flex items-center font-medium text-indigo-500">
      1. Databases <fluent:database-20-filled class="ml-2" />
    </div>
  </li>
  <li>
    <div class="flex items-center font-medium text-blue-500">
      2. Go Programming Basics <vscode-icons:file-type-go-lightblue class="ml-2" />
    </div>
  </li>
  <li>
    <div class="flex items-center font-medium text-blue-400">
      3. REST API in Go <mdi:server class="ml-2" />
    </div>
  </li>
</ul>

<style>
ul {
  list-style-type: none;
}
</style>

---

# What is backend?

Backend is the complex logic that the users does not see

<div class="flex items-start">

<img v-click src="https://cdn.guru99.com/images/1/091318_0717_WhatisBacke1.png" />

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
    width: "100%";
  }
</style>
```

```ts
const express = require("express");
const app = express();
const port = 3000;

app.get("/users/:userId/books/:bookId", function (req, res) {
  const result = db.fetch("...");
  res.send(result);
});
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

# Databases

Why is databases so important?

---

# Types of Databases

There are a lot of different types of databases, two of the most popular are SQL and NoSQL

<img v-click src="https://www.edureka.co/blog/content/ver.1554115042/uploads/2019/04/Examples-of-SQL-and-NoSQL-SQL-vs-NoSQL-Edureka.png" class="w-full" />

<p v-click class="flex items-center">The question is which one should we use? <noto:thinking-face class="ml-2" /></p>

---

# SQL vs NoSQL


<div class="grid grid-cols-2 gap-x-4">

<div>
  <p class="font-bold text-2xl">SQL</p>

  <p class="text-sm text-true-gray-500">follows `Relational Data Model`</p>

  <p>Pros</p>
  <ul>
    <li>Easy to use and setup</li>
    <li>The go-to choice for most application</li>
    <li>Relationships with table joins</li>
    <li>Data are structured</li>
    <li>SQL is powerful</li>
  </ul>

  <p>Cons</p>
  <ul>
    <li>High level of entry (Need to learn a lot of concepts)</li>
    <li>Can be difficult to scale</li>
  </ul>
</div>


<div>
  <p class="font-bold text-2xl">NoSQL</p>

  <p class="text-sm text-true-gray-500">follows `Document Data Model`</p>

  <p>Pros</p>
  <ul>
    <li>No investment in design model</li>
    <li>Generally faster than SQL</li>
    <li>Rapid development cycles</li>
    <li>Run wells in the cloud</li>
    <li>Simpler structure</li>
  </ul>

  <p>Cons</p>
  <ul>
    <li>No relationships</li>
    <li>Not as matured as SQL</li>
  </ul>
</div>

</div>

---
layout: center
class: text-center
---

# Live Coding!

[Click me to enter Replit 💻](https://replit.com/join/jsclkvzqqe-kaiyangyang1)
