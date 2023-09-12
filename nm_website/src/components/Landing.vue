<template>
<div>
<main>
  <section class="products">
    <div class="container">
      <h2>Unsere Produkte</h2>
      <p>Entdecken Sie unsere Produkte</p>
      <router-link to="/produkte" class="btn btn-primary">Produkte anzeigen</router-link>
    </div>
  </section>
  <section class="blog">
  <div class="container">
    <h2>Blog</h2>
    <p>Über die Herstellung unserer Produkte</p>
    <router-link to="/ueber-uns" class="btn btn-primary">Blog aufrufen</router-link>
  </div>
  </section>
  <section class="about">
    <div class="container">
      <h2>Über uns</h2>
      <p>Erfahren Sie mehr über uns</p>
      <router-link to="/ueber-uns" class="btn btn-primary">Über uns erfahren</router-link>
    </div>
  </section>
</main>
<footer>
  <p>&copy; 2023 Natamara. Alle Rechte vorbehalten.</p>
</footer>
</div>
</template>

<script>
export default {
  name: 'LandingPage',
}
</script>

<style scoped>
.container {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}

.btn {
  display: inline-block;
  padding: 10px 20px;
  margin-top: 10px;
  text-decoration: none;
  color: #fff;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.btn-primary {
  background-color: #41b883;
}

</style>