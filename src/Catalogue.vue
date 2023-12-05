<script>
    import CatalogueItem from './components/CatalogueItem.vue'

    export default {
        components: {
        CatalogueItem, 
        },
        data() {
    return {
      products: [
        {name: "Test1", description: "awdaew", price: "1,00€", 
        imageUrls: ["src/assets/logo_small.svg", "src/assets/logo_small_red.svg"],
        colors: ["blue", "green"]},
         
        {name: "Test2", description: "awdawdaew", price: "3,00€", 
         imageUrls: ["src/assets/logo_small.svg", "src/assets/logo_small_red.svg", "src/assets/logo_small_blue.svg"],
         colors: ["blue", "green", "red"]},
        {name: "Test3", description: "awdaawadaew", price: "2,00€", 
         imageUrls: ["src/assets/logo_small.svg", "src/assets/logo_small_red.svg"],
         colors: ["blue", "green"]},
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
      :description="x.description"
      :price="x.price"
      :imageUrls ="x.imageUrls"
      :colors = "x.colors" />
    </div>
  </main>
</template>

<style scoped>
  #wrapper {
    display: flex;
    flex-wrap: wrap;
  }
  #wrapper > div {
    flex-basis: 120px;
    margin: 12px;
    padding: 12px;
  }
</style> 