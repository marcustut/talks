---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: black
# apply any windi css classes to the current slide
class: "text-center"
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# persist drawings in exports and build
drawings:
  persist: false
fonts:
  # basically the text
  sans: "Robot"
  # use with `font-serif` css class from windicss
  serif: "Robot Slab"
  # for code blocks, inline code, etc.
  mono: "Fira Code"
---

# React Workshop

Frontend Web Development with React

<div class="abs-tr !mx-6 !my-8 flex flex-col animate-pulse">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a7/React-icon.svg/2300px-React-icon.svg.png" class="w-12 m-auto rounded-lg">
</div>

<div class="abs-bl !mx-14 my-12 flex flex-col">
  <div class="mb-3 uppercase tracking-widest font-medium">
  Marcus Lee
  </div>
  <div class="text-md opacity-50">Year 3 Software Engineering Student @ TARUC</div>
</div>

<style>
  div {
    @apply text-left font-sans;
  }
</style>

<!--
-->

---
layout: intro
---

# Marcus Lee

<div class="opacity-80">
  <div class="inline flex items-center">Coming Software Engineering Intern at <a class="flex items-center ml-1 opacity-70" href="https://www.y2123.com/" target="_blank">Y2123<img class="w-4 h-4 ml-1" src="https://static.wixstatic.com/media/222aae_c6a81ef9965c473cb7f2e2544da311fc~mv2.png/v1/fill/w_32%2Ch_32%2Clg_1%2Cusm_0.66_1.00_0.01/222aae_c6a81ef9965c473cb7f2e2544da311fc~mv2.png" /></a></div><br>
  <div class="inline flex items-center">Had 1 year experience as Tech Lead at <a class="flex items-center ml-1 opacity-70" href="https://www.lsmachinery.com.my/" target="_blank">LS Smart Machinery<img class="w-4 h-4 ml-1" src="https://www.lsmachinery.com.my/favicon.ico" /></a></div><br>
  Love and contribute to open-source<br>
</div>

<div class="my-10 grid grid-cols-[40px,1fr] w-max gap-y-4">
  <ri-github-line class="opacity-50"/>
  <div><a href="https://github.com/marcustut" target="_blank">marcustut</a></div>
  <ri-instagram-line class="opacity-50"/>
  <div><a href="https://instagram.com/geminimarcus" target="_blank">geminimarcus</a></div>
  <ri:linkedin-box-line class="opacity-50"/>
  <div><a href="https://www.linkedin.com/in/geminimarcus/" target="_blank">Marcus Lee</a></div>
</div>

<img src="https://avatars.githubusercontent.com/u/59773847?v=4" class="rounded-full w-40 h-40 object-cover abs-tr mt-16 mr-12"/>

<style>
  a {
    @apply hover:text-neutral-200 hover:opacity-100
  }
</style>

---
layout: center
---

# Table of Contents

<ul class="list-none">
  <li>
    <div class="flex items-center font-medium text-blue-400">
      1. <logos:react class="mx-2" /> Showcase
    </div>
  </li>
  <li>
    <div class="flex items-center font-medium text-indigo-400">
      2. Origins of JavaScript <noto-v1:open-book class="ml-2" />
    </div>
  </li>
  <li>
    <div class="flex items-center font-medium text-yellow-300">
      3. Introduction to <logos:javascript class="ml-2" />
    </div>
  </li>
  <li>
    <div class="flex items-center font-medium text-yellow-400">
      4. ES6 Syntax and Why it is important <noto-v1:thinking-face class="ml-2" />
    </div>
  </li>
  <li>
    <div class="flex items-center font-medium text-red-400">
      5. React Theory <noto:brain class="ml-2" />
    </div>
  </li>
  <li>
    <div class="flex items-center font-medium text-amber-500">
      6. Your first React Application <noto-v1:fire class="ml-2" />
    </div>
  </li>
</ul>

<style>
h1 {
  @apply text-neutral-200;
}
ul {
  list-style-type: none;
}
</style>

---
layout: image-right
image: 
---

# What is frontend?

Frontend is basically what you see and what you interact with!

<div class="flex items-start">

<Tweet id="1402320383932502021" />
<Counter :count="10" class="ml-3 mt-3" />

</div>

<style>
h1 {
  @apply text-neutral-200;
}
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

---
layout: center
---

<h1 class="text-transparent bg-clip-text bg-gradient-to-r from-green-500 to-blue-500">Showcase Time!</h1>

<Confetti />

<style>
</style>

---
## class: px-20
---

# Origins of JavaScript

In September 1995, a Netscape programmer named Brandan Eich developed a new scripting language in just 10 days. It was originally named Mocha, but quickly became known as LiveScript and, later, JavaScript.

<div grid="~ cols-2 gap-2" m="-t-2">

<img v-click border="rounded" src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/08/Netscape_icon.svg/1200px-Netscape_icon.svg.png">

<img v-click border="rounded" src="https://upload.wikimedia.org/wikipedia/commons/2/29/Windows_Internet_Explorer_Logo.png">

</div>

<style>
  h1 {
    @apply text-neutral-200;
  }
</style>

---

<img border="rounded" src="https://inteng-storage.s3.amazonaws.com/images/import/2017/08/oldestwebsites9.jpg" />

<p v-click class="absolute p-3 bg-green-500 font-bold right-24 bottom-8">The Web is originally meant for docs!</p>

---

<img border="rounded" src="https://hips.hearstapps.com/hmg-prod.s3.amazonaws.com/images/ebay-website-old-1572631752.png?resize=480:*" />

<p v-click class="absolute p-3 bg-indigo-800 font-bold right-24 top-8">👈🏼 JavaScript allowed this</p>

---

# A Taste of JavaScript

JavaScript can do a lot of cool stuff.

<div class="grid grid-cols-3 gap-10 pt-4 -mb-6">

</div>

[JavaScript Playground](https://codesandbox.io/s/introduction-to-javascript-8tncwl?file=/src/index.js)

<style>
  h1 {
    @apply text-neutral-200;
  }
</style>

---

# JavaScript Syntax

<div class="grid grid-cols-2 gap-10">

```js
// Variables
const b = 10;

var x = 5;
var name = "Marcus Lee";
var price = 5.2

let y = 3;
let name2 = "Jordan Tan";
let price2 = 4.5
```

```js
// Functions
function add(a, b) {
  return a + b;
}

function sayMyName(name) {
  console.log(`hello, ${name}!`);
}
```

</div>

<div class="grid grid-cols-2 gap-10 pt-4">

```js
// Class
class Dog {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
}
const myDog = new Dog("Happy", 3);
```

```js
// Manipulating the DOM
document.getElementById("demo").innerHTML = "Hi John!";

document.getElementById("demo").style.display = "none";
```

</div>

[JavaScript Playground](https://codesandbox.io/s/introduction-to-javascript-8tncwl?file=/src/index.js)

<style>
  h1 {
    @apply text-neutral-200;
  }
</style>

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

<style>
  h1 {
    @apply text-neutral-200;
  }
</style>

<!--
I won't go too details about ES6, there are much more about it you can find online
  I'll go through the biggest change and particularly focusing on 'Data parsing'
  This is important because we need ES6 to start exploring on React
-->

---
layout: center
class: text-center
---

# React, apatu?!?? 🤔

<p v-click class="opacity-80">React is a declarative, efficient, and flexible JavaScript library for building user interfaces.</p>

<style>
  h1 {
    @apply text-neutral-200;
  }
</style>

---

# Vanilla JS vs React

Below shows a comparison between building UI with React and Vanilla JS.

<div class="grid grid-cols-2 gap-x-4">

```js
// Vanilla JavaScript
const data = [
  { name: "Marcus Lee", age: 22, course: 'Bachelor Degree in Software Engineering' },
  { name: "Danny Phang", age: 23, course: 'Bachelor Degree in Graphic Design' },
  { name: "Liana Ling", age: 20, course: 'Bachelor Degree in Software Engineering' },
  { name: "Wong Wai Yi", age: 22, course: 'Bachelor Degree in Fashion Design' },
];

// let dataHtml = data.map((d) => `<p>${d.name} is ${d.age} years old and currently pursuing ${d.course}.</p>`);
let dataHtml = data.map(function(d) {
  return `<p>${d.name} is ${d.age} years old and currently pursuing ${d.course}.</p>`;
});

document.getElementById("demo").innerHtml = dataHtml;
```

```jsx
// React
export function App() {
  const [data, setData] = useState([
    { name: "Marcus Lee", age: 22, course: 'Bachelor Degree in Software Engineering' },
    { name: "Danny Phang", age: 23, course: 'Bachelor Degree in Graphic Design' },
    { name: "Liana Ling", age: 20, course: 'Bachelor Degree in Software Engineering' },
    { name: "Wong Wai Yi", age: 22, course: 'Bachelor Degree in Fashion Design' },
  ]);

  return (
    <div>
      <h1>Data Demo</h1>

      {data.map((d) => <p>{`${d.name} is ${d.age} years old and currently pursuing ${d.course}`}</p>)}
    </div>
  )
}
```

</div>

<style>
  h1 {
    @apply text-neutral-200;
  }
</style>

---
layout: center
class: text-center
---

# Build your first React App!

<p v-click class="opacity-80">Theory is nothing, let's experience it by building one ourselves!</p>

<a v-click href="https://codesandbox.io/s/react-workshop-app-e02o2y?file=/src/App.js" target="_blank">Link to CodeSandbox</a>

<style>
  h1 {
    @apply text-neutral-200;
  }
</style>

---
layout: center
class: text-center
---

# Thanks for joining!

Feel free to reach out if you need any help 👇🏼

[WhatsApp](https://wa.me/+60163066883) · [GitHub](https://github.com/marcustut) · [Instagram](https://www.instagram.com/geminimarcus/)
