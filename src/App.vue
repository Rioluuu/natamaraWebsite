<script setup>
import { ref, computed } from 'vue'
import Landing from './Landing.vue'
import Catalogue from './Catalogue.vue'
import About from './About.vue'
import Ingredients from "./Ingredients.vue";

const routes = {
  '/': Landing,
  '/catalogue': Catalogue,
  '/ingredients': Ingredients,
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
  <component :is="currentView" />
  <footer>
    <p>&copy; 2023 Natamara. Alle Rechte vorbehalten.</p>
  </footer>
</template>

