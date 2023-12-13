<script setup>
import LandingButtons from "./components/LandingButtons.vue";
</script>

<template>
  <main>
    <img src="/logo_superlarge.svg" alt="Natamara Logo" class="responsive">
    <LandingButtons/>
  </main>
</template>

<style scoped>
header {
  line-height: 1.3;
}

main {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 95vh;
}
.responsive {
  width: 70%;
  height: auto;
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
