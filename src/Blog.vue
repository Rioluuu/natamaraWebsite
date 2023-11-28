<script>
    import BlogItem from './components/BlogItem.vue'

    export default {
        components: {
        BlogItem, 
        },
        data() {
    return {
      products: [
        {name: "Test1", description: "awdaew", link: "#", imageUrl: "../assets/logo_small.svg"},
        {name: "Test2", description: "awdawdaew", link: "#", imageUrl: "../assets/logo_small.svg"},
        {name: "Test3", description: "awdaawadaew", link: "#", imageUrl: "../assets/logo_small.svg"},
      ]
    };
  }
};
</script>



<template>
  <main style="padding-top:0;padding-bottom:0;">
    <h1>Blog</h1>
  </main>
  <main style="padding: 0">
    <div id="wrapper">
        <BlogItem  v-for="x in products"
      :name ="x.name"
      :description="x.description"
      :link="x.link"
      :imageUrl="x.imageUrl" />
    </div>
  </main>
</template>

<style scoped>
  #wrapper > div {
    margin: 12px;
    padding: 12px;
  }
</style> 