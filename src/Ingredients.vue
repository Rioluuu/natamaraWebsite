<script>
    import IngredientItem from './components/IngredientItem.vue'
    import NavBar from "@/components/NavBar.vue";

    export default {
        components: {
          NavBar,
        IngredientItem,
        },
        data() {
    return {
      products: [
        {name: "Seife", price: "5,00€",
        imageUrls: ["src/assets/logo_small.svg", "src/assets/logo_small_red.svg", "src/assets/logo_small_blue.svg", "src/assets/logo_small_red2.svg"],
        colors: ["#d9c022", "#ffa500", "#967BB6", "#d32a4a"],
        descriptions: ["Zitrone", "Orange", "Lavendel", "Bratapfel"],
        ingredients: ["Kokosöl, Olivenöl, Rapsöl, Mandelöl, Avocadoöl, Kakaobutter, Bienenwachs, Sheabutter, ätherische Öle, Seifenpigment",
          "Kokosöl, Olivenöl, Rapsöl, Mandelöl, Avocadoöl, Kakaobutter, Bienenwachs, Sheabutter, ätherische Öle, Seifenpigment",
          "Kokosöl, Olivenöl, Rapsöl, Mandelöl, Avocadoöl, Kakaobutter, Bienenwachs, Sheabutter, ätherische Öle, Seifenpigment",
          "Kokosöl, Olivenöl, Rapsöl, Mandelöl, Avocadoöl, Kakaobutter, Bienenwachs, Sheabutter, ätherische Öle, Seifenpigment"]},
      
        {name: "Handcreme", price: "4,00€",
         imageUrls: ["src/assets/logo_small.svg"],
         colors: ["blue"],
        descriptions: ["Aloe vera"],
        ingredients: ["Olivenöl, Tegomuls, Bienenwachs, Cetylalkohol, Urea"]},

        {name: "Lippenbalsam", price: "2,00€",
         imageUrls: ["src/assets/logo_small.svg"],
         colors: ["blue"],
        ingredients: ["Rapsöl, Jojobaöl, Kakaobutter, Bienenwachs, Aloe Vera, Panthenol"]},

        {name: "Peelings", price: "7,50€",
          imageUrls: ["src/assets/logo_small.svg", "src/assets/logo_small_red.svg", "src/assets/logo_small_blue.svg", "a"],
          colors: ["#727b6c", "#d9c022", "#967BB6", "#6b9e49"],
          descriptions: ["Zitrone-Thymian", "Rosmarin-Zitrone", "Lavendel", "Rosmarin"],
          ingredients: ["Salz, Olivenöl, Zitrone, Thymian", "Zucker, Olivenöl, Rosmarin, Zitrone", "Zucker, Mandelöl, Lavendelblüten, Lavendel-Öl", "Zucker, Olivenöl, Rosmarin"]},
      ]
    };
  }
};
</script>



<template>
  <NavBar />
  <main style="padding-top:0;padding-bottom:0;">
    <h1>Inhaltsstoffe</h1>
    <a href="#/catalogue"><u>» zum Katalog</u></a>
  </main>
  <main style="padding: 0">
    <div id="wrapper">
        <IngredientItem  v-for="x in products"
      :name ="x.name"
      :price="x.price"
      :imageUrls ="x.imageUrls"
      :colors = "x.colors"
      :descriptions="x.descriptions"
      :ingredients="x.ingredients"/>
    </div>
  </main>
</template>

<style scoped>
  #wrapper {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
  }
  #wrapper > div {
    flex: 1;
    margin: 12px;
    padding: 12px;
    box-sizing: border-box;
    max-width: 400px;
  }
</style> 