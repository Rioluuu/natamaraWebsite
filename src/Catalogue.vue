<script>
    import CatalogueItem from './components/CatalogueItem.vue'

    export default {
        components: {
        CatalogueItem, 
        },
        data() {
    return {
      products: [
        {name: "Test1", description: "awdaew", imageUrl: "../assets/logo_small.svg"},
        {name: "Test2", description: "awdawdaew", imageUrl: "../assets/logo_small.svg"},
        {name: "Test3", description: "awdaawadaew", imageUrl: "../assets/logo_small.svg"},
      ]
    };
  }
};
</script>



<template>
    <h1>Katalog</h1>
    <div id="wrapper">
        <CatalogueItem  v-for="x in products"
      :name ="x.name"
      :description="x.description"
      :imageUrl="x.imageUrl" />
    </div>
    
</template>

<style scoped>
  #wrapper {
    display: flex;
    flex-wrap: wrap;
  }
  #wrapper > div {
    flex-basis: 120px;
    margin: 10px;
    padding: 10px;
  }
</style> 