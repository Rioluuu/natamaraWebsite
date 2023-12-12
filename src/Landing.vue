<script setup>
import LandingButtons from "./components/LandingButtons.vue";
import NavBar from "@/components/NavBar.vue";
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

.responsive {
  width: 70%;
  height: auto;
  display: block;
  margin-left: auto;
  margin-right: auto;
  margin-top: 5%;
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
