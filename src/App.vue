<script setup>
import { ref, computed } from 'vue'
import Landing from './Landing.vue'
import Blog from './Blog.vue'
import Catalogue from './Catalogue.vue'

const routes = {
  '/': Landing,
  '/blog': Blog,
  '/catalogue': Catalogue
}

const currentPath = ref(window.location.hash)

window.addEventListener('hashchange', () => {
  currentPath.value = window.location.hash
})

const currentView = computed(() => {
  return routes[currentPath.value.slice(1) || '/'] || NotFound
})
</script>

<template>
  <a href="#/">Home</a> | <a href="#/blog">Blog</a> | <a href="#/catalogue">Katalog</a>
  <component :is="currentView" />
</template>