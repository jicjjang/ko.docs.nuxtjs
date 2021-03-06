---
title: 프리프로세서
description: Nuxt.js 에서 프리프로세서를 사용하려면?
---

<!-- title: Pre-processors -->
<!-- description: How to use pre-processors with Nuxt.js? -->

<!-- # How to use pre-processors? -->

# 프리프로세서를 사용하려면?

<!-- Thanks to [vue-loader](http://vue-loader.vuejs.org/en/configurations/pre-processors.html), you can use any kind of pre-processors for your `<template>`, `<script>` or `<style>`: simply use the `lang` attribute. -->

[vue-loader](http://vue-loader.vuejs.org/en/configurations/pre-processors.html) 덕뿐에 그냥 `lang` 속성을 사용하는 것만으로 `<template>`, `<script>`, `<style>` 을 위한 프리프로세서를 사용할 수 있습니다.

<!-- Example of our `pages/index.vue` using [Pug](https://github.com/pugjs/pug), [CoffeeScript](http://coffeescript.org) and [Sass](http://sass-lang.com/): -->

[Pug](https://github.com/pugjs/pug), [CoffeeScript](http://coffeescript.org), [Sass](http://sass-lang.com/) 를 사용한 `pages/index.vue` 예제:

```html
<template lang="pug">
  h1.red Hello {{ name }}!
</template>

<script lang="coffee">
module.exports = data: ->
  { name: 'World' }
</script>

<style lang="sass">
.red
  color: red
</style>
```

<!-- To be able to use these pre-processors, we need to install their webpack loaders: -->

이런 프리프로세서를 사용하기 위해서는 Webpack 로더들을 설치해야 합니다.

```bash
npm install --save-dev pug@2.0.0-beta6 pug-loader coffee-script coffee-loader node-sass sass-loader
```
