<template>
    <div class="shop-item">
      <img src="../assets/logo_small.svg" class="item-image" alt="kleines Natamara-Logo">
      <h2 class="item-name">{{ name }}</h2>
      <p class="item-description">{{ description }}</p>
      <h2 class="item-price">{{ price }}</h2>
    </div>
  </template>
  
  <script>
    export default {
        props: {
            name: String,
            description: String,
            price: String,
            imageUrl: String,
        }
    }
  </script>
  
  <style scoped>
  .shop-item {
    border: 0;
    border-radius: 12px;
    padding: 16px;
    text-align: center;
    background-color: #ece7ca;
    box-shadow: 0 0 6px #c9c29f;
  }
  
  .item-image {
    height: auto;
    width: 20rem;
  }
  
  .item-name {
    font-size: 1.5rem;
    margin: 8px 0;
  }
  
  .item-description {
    text-align: left;
    margin: 8px 0;
    float: left;
  }

  .item-price {
    float: right;
    font-weight: bold;
  }
  </style>
  