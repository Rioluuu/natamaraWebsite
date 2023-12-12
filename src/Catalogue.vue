<script>
    import CatalogueItem from './components/CatalogueItem.vue'
    import NavBar from "@/components/NavBar.vue";

    export default {
        components: {
          NavBar,
          CatalogueItem,
        },
        data() {
    return {
      products: [
        {name: "Seife", price: "5,00€",
        imageUrls: ["src/assets/Produktbilder/SeifeZitrone.jpg", "src/assets/Produktbilder/SeifeOrange.jpg", "src/assets/Produktbilder/SeifeLavendel.jpg", "src/assets/Produktbilder/SeifeBratapfel.jpg"],
        colors: ["#d9c022", "#ffa500", "#967BB6", "#d32a4a"],
        descriptions: ["Zitrone", "Orange", "Lavendel", "Bratapfel"]},
      
        {name: "Handcreme", price: "4,00€",
         imageUrls: ["src/assets/Produktbilder/HandCremeKlein.jpg"],
         colors: ["white"],
        descriptions: ["Aloe vera"]},

        {name: "Lippenbalsam", price: "2,00€",
         imageUrls: ["src/assets/Produktbilder/HandCremeGroß.jpg"],
         colors: ["white"],
         descriptions: [" "]},

        {name: "Peelings", price: "7,50€",
          imageUrls: ["src/assets/Produktbilder/Peeling1.jpg", "src/assets/Produktbilder/Peeling2.jpg", "src/assets/Produktbilder/Peeling3.jpg", "src/assets/Produktbilder/Peeling4.jpg"],
          colors: ["#727b6c", "#6b9e49", "#d9c022", "#967BB6"],
          descriptions: ["Zitrone-Thymian", "Rosmarin", "Zitrone-Rosmarin", "Lavendel"]},

        {name: "Kerzen", price: "5,00€",
          imageUrls: ["src/assets/Produktbilder/RoteKerze.jpg", "src/assets/Produktbilder/GrueneKerze.jpg", "src/assets/Produktbilder/OrangeKerze.jpg"],
          colors: ["red", "green", "orange"],
          descriptions: ["rot", "grün", "orange"]},
      ]
    };
  }
};
</script>



<template>
  <NavBar />
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