<script setup>
import LandingButtons from "./components/LandingButtons.vue";
</script>

<template>
  <main>
    <LandingButtons/>
  </main>
</template>

<style scoped>
header {
  line-height: 1.3;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

}
</style>
