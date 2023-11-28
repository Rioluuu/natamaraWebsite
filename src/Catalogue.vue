<script>
    import CatalogueItem from './components/CatalogueItem.vue'

    export default {
        components: {
        CatalogueItem, 
        },
        data() {
    return {
      products: [
        {name: "Test1", description: "awdaew", price: "1,00€", imageUrl: "../assets/logo_small.svg"},
        {name: "Test2", description: "awdawdaew", price: "3,00€", imageUrl: "../assets/logo_small.svg"},
        {name: "Test3", description: "awdaawadaew", price: "2,00€", imageUrl: "../assets/logo_small.svg"},
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
      :imageUrl="x.imageUrl" />
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