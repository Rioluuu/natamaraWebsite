<template>
  <main>
    <h1>Über uns</h1>
    <div class="about-us">
      <section class="history">
        <h2>Unsere Gründungsgeschichte</h2>
        <p>
          Hier können Sie Ihre Gründungsgeschichte oder Hintergrundinformationen über Ihr Unternehmen oder Team hinzufügen.
        </p>
      </section>

      <section class="team-photo">
        <h2>Unser Team</h2>
        <!-- <img src="assets/gruppenfoto.jpg" alt="Unser Team" /> -->
      </section>

      <section class="product-ideas">
        <h2>Unsere Produktideen</h2>
        <ul>
          <li>Seife: Wie letztes Jahr bieten wir wieder Seife </li>
          <li>Handcreme: Beschreibung der zweiten Produktidee.</li>
          <li>Labelo: Beschreibung der dritten Produktidee.</li>
          <li>Peelings: </li>
          <!-- Fügen Sie weitere Produktideen nach Bedarf hinzu -->
        </ul>
      </section>
    </div>
  </main>

</template>

<script>
export default {
  name: "AboutUs",
};
</script>

<style scoped>
/* Fügen Sie hier Ihr CSS-Styling hinzu, um die Seite anzupassen */
.about-us {
  /* Stil für die Gesamtseite */
}

.history {
  /* Stil für den Abschnitt mit der Gründungsgeschichte */
}

.team-photo {
  /* Stil für den Abschnitt mit dem Gruppenfoto */
}

.product-ideas {
  /* Stil für den Abschnitt mit den Produktideen */
}
</style>
