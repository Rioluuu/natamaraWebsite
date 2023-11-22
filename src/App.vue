<script setup>
import { ref, computed } from 'vue'
import Landing from './Landing.vue'
import Blog from './Blog.vue'
import Catalogue from './Catalogue.vue'
import About from './About.vue'
import NavBar from './components/NavBar.vue'

const routes = {
  '/': Landing,
  '/blog': Blog,
  '/catalogue': Catalogue,
  '/about': About
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
  <NavBar />
  <component :is="currentView" />
  <footer>
    <p>&copy; 2023 Natamara. Alle Rechte vorbehalten.</p>
  </footer>
</template>

