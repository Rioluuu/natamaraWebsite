<template>
    <div class="shop-item">
      <img src="../assets/logo_small.svg" class="item-image">
      <h2 class="item-name">{{ name }}</h2>
      <p class="item-description">{{ description }}</p>
    </div>
  </template>
  
  <script>
    export default {
        props: {
            name: String,
            description: String,
            imageUrl: String,
        }
    }
  </script>
  
  <style scoped>
  .shop-item {
    border: 1px solid #ccc;
    padding: 16px;
    text-align: center;
  }
  
  .item-image {
    height: auto;
    width: 30rem;
  }
  
  .item-name {
    font-size: 1.5rem;
    margin: 8px 0;
  }
  
  .item-description {
    margin: 8px 0;
  }
  </style>
  