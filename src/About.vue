<template>
  <main>
    <h1>Über uns</h1>
    <div class="about-us">
      <section class="history">
        <h2>Unsere Gründungsgeschichte</h2>
        <p>
          Wir haben die Natamara Schülerfirma im Rahmen des Seminarfaches von Frau Stäudte gebildet.<br>
          Unsere Grundidee sind qualitative und nachhaltige Produkte von Schülern für Schüler und Eltern.<br>
          Begonnen haben wir mit einer Namensfindung und möglichen Produkten, wie zum Beispiel Badebomben und Deo neben unseren vorhandenen Katalog.<br>
          Natamara stellt sich in diesem Fall aus Natürlich und "Amara", welches aus dem {Sprache} kommt und etwas natürliches Symbolisiert.<br>
          Jeder Kauf unterstützt unsere Abikasse!
        </p>
      </section>

      <section class="team-photo">
        <h2>Unser Team</h2>
        <p>
          Wir haben unsere Aufgabengebiete wie folgt aufgeteilt, um effizienter arbeiten zu können und unsere eigenen Stärken bestmöglichst einzusetzen:<br><br>
          Geschäftsführung: Celine, Jenna<br>
          IT: Christian, Maurice, Thomas<br>
          Finanzen/Rechtsabteilung: Malik, Karlotta, Kathleen, Annika<br>
          Design/Marketing: Jannik, Lisa, Johann, Mohammed, Jasper<br>
          Rezeptur: Jenna, Paul, Mika, Nicolas<br><br>
          betreuende Lehrkraft: Andrea Stäudte
        </p>
        <!-- <img src="assets/gruppenfoto.jpg" alt="Unser Team" /> -->
      </section>

      <section class="product-ideas">
        <h2>Unsere Produktideen</h2>
        <ul>
          <li>Seife: {Rezeptur} </li>
          <li>Handcreme: {Rezeptur}</li>
          <li>Labelo: {Rezeptur}</li>
          <li>Peelings: {Rezeptur} </li>
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
