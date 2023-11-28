<template>
    <main>
    <div class="block">
        <h1 class="title">{{ title }}</h1>
        <p class="date">{{ date }}</p>
        <p class="mainbody">{{ body }}</p>
        <div class="images">
        <image class="image1"></image>
        <image class="image2"></image>
        <image class="image3"></image>
        </div>
    </div>
    </main>
</template>
  
  <script>
    export default {
        props: {
            title: String,
            body: String,
            image1Url: String,
            image2Url: String,
            image3Url: String,
            date: String,
        }
    }
  </script>
  
  <style scoped>
  .block{
    display:grid;
    grid-template-columns: 5% 50% 30%;
    grid-template-rows: 30px 20px 20 px auto;
    grid-template-areas:
    ". title ."
    ". . ."
    ". date ."
    ". body image"
  }
  .block-item{
    padding: 0px;
  }
  .title{
    grid-area: title;
  }
  .date{
    grid-area: date;
  }
  .images{
    grid-area: image;
  }
  image1{
    background-image: v-bind('image1');
  }
  image2{
    background-image: v-bind('')
  }
  image3{
    background-image: v-bind('')
  }
  .mainbody{
    grid-area: body;
  }
  
  
  </style>
  