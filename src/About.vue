<template>
  <NavBar />
  <main>
    <h1>Über uns</h1>
    <div class="About">
      <section class="Text">
        <h2>Unsere Gründungsgeschichte</h2>
          <p>Wir haben die Natamara Schülerfirma im Rahmen des Seminarfaches von Frau Stäudte gebildet.</p>
          <p>Unsere Grundidee sind qualitative und nachhaltige Produkte von Schülern für Schüler und Eltern.</p>
          <p>Begonnen haben wir mit einer Namensfindung und möglichen Produkten, wie zum Beispiel Badebomben und Deo neben unseren vorhandenen Katalog.</p>
          <p>Natamara stellt sich in diesem Fall aus Natürlich und "Amara", welches aus dem Asiatischen kommt und etwas natürliches Symbolisiert.</p>
          <p>Jeder Kauf unterstützt unsere Abikasse!</p>
      </section>

      <section class="Text">
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
      </section>

      <section>
        <h2>Unsere Produktideen</h2>
        <ul>
          <li>Seife</li>
          <li>Handcreme</li>
          <li>Labelo</li>
          <li>Peelings</li>
        </ul>
        <img src="../src/assets/PXL_20231212_143110340~2.jpg" class="Bild">
      </section>
    </div>
  </main>

</template>

<script>
import NavBar from "@/components/NavBar.vue";

export default {
  name: "AboutUs",
  components: {NavBar},
};
</script>

<style scoped>
.Bild {
  border-radius: 12px;
  max-width: 400px;
  max-height: 150px;
}
.About{
  max-width: 100%;
  max-height: 100%;
}
.Text{
  max-width: 75%;
  max-height: 75%;
}
</style>
