<script>
    import CatalogueItem from './components/CatalogueItem.vue'

    export default {
        components: {
        CatalogueItem, 
        },
        data() {
    return {
      products: [
        {name: "Seife", price: "5,00€",
        imageUrls: ["src/assets/logo_small.svg", "src/assets/logo_small_red.svg", "src/assets/logo_small_blue.svg", "src/assets/logo_small_red2.svg"],
        colors: ["blue", "green", "red", "orange"],
        descriptions: ["Lavendel", "Zitrone", "Orange", "Bratapfel"]},
      
        {name: "Handcreme", price: "4,00€",
         imageUrls: ["src/assets/logo_small.svg"],
         colors: ["blue"],
        descriptions: ["Aloe vera"]},

        {name: "Lippenbalsam", price: "2,00€",
         imageUrls: ["src/assets/logo_small.svg"],
         colors: ["blue"],
         descriptions: [" "]},

        {name: "Peelings", price: "7,50€",
          imageUrls: ["src/assets/logo_small.svg", "src/assets/logo_small_red.svg", "src/assets/logo_small_blue.svg"],
          colors: ["blue", "green", "red"],
          descriptions: ["Zitrone-Thymian", "Zucker-Rosmarin", "Lavendel"]},

        {name: "Kerzen", price: "5,00€",
          imageUrls: ["src/assets/logo_small.svg", "src/assets/logo_small_red.svg", "src/assets/logo_small_blue.svg"],
          colors: ["red", "green", "yellow"],
          descriptions: ["rot", "grün", "gelb"]},
      ]
    };
  }
};
</script>



<template>
  <main style="padding-top:0;padding-bottom:0;">
    <h1>Katalog</h1>
  </main>
  <main style="padding: 0">
    <div id="wrapper">
        <CatalogueItem  v-for="x in products"
      :name ="x.name"
      :price="x.price"
      :imageUrls ="x.imageUrls"
      :colors = "x.colors"
      :descriptions="x.descriptions" />
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