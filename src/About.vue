<template>
  <NavBar />
  <main>
    <h1>Über uns</h1>
    <div class="About">
      <section class="Text">
        <section class="Subtext">
        <h2>Unsere Gründungsgeschichte</h2>
          Wir haben die Natamara Schülerfirma im Rahmen des Seminarfaches von Frau Stäudte gebildet.
          Unsere Grundidee sind qualitative und nachhaltige Produkte von Schülern für Schüler und Eltern.
          Begonnen haben wir mit einer Namensfindung und möglichen Produkten, wie zum Beispiel Badebomben und Deo neben unseren vorhandenen Katalog.
          Natamara stellt sich in diesem Fall aus Natürlich und "Amara", welches aus dem Asiatischen kommt und etwas natürliches Symbolisiert.
          Jeder Kauf unterstützt unsere Abikasse!
        </section>
        <h2>Unser Team</h2>
        <section class="Subtext">
        <p>
          Wir haben unsere Aufgabengebiete wie folgt aufgeteilt, um effizienter arbeiten zu können und unsere eigenen Stärken bestmöglichst einzusetzen:<br>
          <ul>
          <li>Geschäftsführung: Celine Rutz, Jenna Allenbach</li>
          <li>IT: Christian Pordzig, Maurice Schulz, Thomas Gerlin</li>
          <li>Finanzen/Rechtsabteilung: Malik Strohbach, Karlotta Dunecke, Kathleen Meyer, Annika Matschull</li>
          <li>Design/Marketing: Jannik Zey, Lisa Abram, Johann Hünecke, Mohammed Abbas, Jasper Reich</li>
          <li>Rezeptur: Jenna Allenbach, Paul Grzywna, Mika Knief, Nicolas Schmid</li>
          <li>Helfer: Christoph Klein, Jan Wassiljew, Niels Schulte, Leon Kuhn</li>
          <li>betreuende Lehrkraft: Andrea Stäudte</li>
          </ul>

          Jeder hat bei der Produktion und Verpackung geholfen, sonst könnte der Verkauf niemals stattfinden!
        </p>
        </section>
        <h2>Unsere Produkte</h2>
        <ul>
          <li>Seife</li>
          <li>Handcreme</li>
          <li>Peelings</li>
        </ul>
        <img src="../src/assets/Produktbilder/ProduktGruppenFoto.jpg" class="Bild">
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
  max-width: 600px;
  max-height: Auto;
}
.About{
  max-width: 100%;
  max-height: 100%;
  border: 0;
  border-radius: 12px;
  padding: 16px;
  text-align: center;
  background-color: #ece7ca;
  box-shadow: 0 0 6px #c9c29f;
}
.Text{
  max-width: 75%;
  max-height: 75%;
  text-align: left;
}
.Subtext{
  max-width: 700px;
  line-height: 25px;
  hyphens: auto;
  text-align: justify;
}
h2{
  margin-top: 10px;
}
</style>
