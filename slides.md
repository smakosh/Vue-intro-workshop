---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://images.unsplash.com/photo-1496304841270-2cb66cf766b4?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80
# apply any windi css classes to the current slide
class: 'text-center'
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
---

# Introduction to Vue js

A short and quick intro to Vue js

<div class="abs-br m-6 flex gap-2">
  <a href="https://github.com/smakosh" target="_blank" alt="GitHub"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

---
layout: image-right
image: https://images.unsplash.com/photo-1558281831-9118ac25b581?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1074&q=80
---

# But, who are you?

- I'm Ismail, known as Smakosh on the web.
- A self-taught designer & developer
- I made few products, some are online like [Ontwik](https://ontwik-dev.com), others are dead like [Beaf](https://github.com/smakosh?tab=repositories&q=beaf&type=&language=&sort=) while the rest are sinking like [Ai Hashtags](https://ai-hashtags.com)
- OSS developer and blogger, you can find me on GitHub or Twitter under the username [Smakosh](https://smakosh.com)
- Huge fan of tech, finance, crypto, sci-fi and anime

---
layout: two-cols
---

# So, what is Vue.js?

A JavaScript framework that lets you build web UIs, its core concepts are:

- Vue instances
- SFC (Single file components)
  - template
  - script
  - style
- Vue directives
- State (data)
- Methods (default lifecycle hooks)
> Lifecycle methods are called outside the "methods" object.

::right::

```js
<template>
  <div id="app">
    <input name="name" v-model="name" />
    {{name}}
  </div>
</template>

<script>
export default {
  name: "App",
  data: function () {
    return {
      name: "",
    };
  },
  methods: {
    handleName: function (event) {
      this.name = event.target.value;
    },
  }
};
</script>

<style>
#app {
  color: #2c3e50;
}
</style>
```

---

# Vue directives

### Piece of code that get binded to a certain DOM element or component

|     |     |
| --- | --- |
| <kbd>v-show</kbd> | show an element if certain condition is met but it's still in the DOM |
| <kbd>v-bind</kbd> | binds one or more attributes to a DOM element or a component prop to an element |
| <kbd>v-on</kbd> | Lets you listen to DOM events to run some JavaScript when the events are triggered  |
| <kbd>v-model</kbd> | Used for binding with form inputs |
| <kbd>v-if / v-if-else / v-else</kbd> | Same thing as v-show except it removes it from the DOM |
| <kbd>v-for</kbd> | Iterate through Arrays and Objects |
| <kbd>v-once</kbd> | Renders the element once and will never change |

---

# Data (state)

```js {3-7|all}
<script>
export default {
  name: "App",
  data: function () {
    return {
      name: "",
    };
  },
  methods: {
    handleName: function (event) {
      this.name = event.target.value;
    },
  }
};
</script>
```

---
layout: two-cols
---

# Methods (with default lifecycle hooks)

- beforeCreate
- created
- beforeMount
- mounted
- beforeUpdate
- updated
- beforeDestroy
- destroyed
  
> You can access any state within these methods using the “this” keyword

::right::

```js
<script>
export default {
  name: "App",
  data: function () {
    return {
      name: "",
    };
  },
  created: function (event) {
    this.name = "created";
  },
  methods: {
    handleName: function (event) {
      this.name = event.target.value;
    },
  }
};
</script>
```

---

# How is Vue different from React js?

- Standard syntax, no new syntax like JSX added to the learning curve
- Style is scoped by default, you wouldn't really need CSS in JS or CSS modules
- Uses Mustache syntax for data binding’s interpolation
- Directives
- Methods
- CLI with customization options
- Vue plugins
- Built-in router as a Vue plugin

---
layout: center
---

# Demo time

---
layout: center
---

# That's all, questions time!

[Documentation](https://v2.vuejs.org/) · [GitHub](https://github.com/smakosh) · [Twitter](https://twitter.com/smakosh) · [Written version](https://smakosh.notion.site/Vue-JS-introduction-d2f826ab7a574eed9a34f7cd01d88fae)
