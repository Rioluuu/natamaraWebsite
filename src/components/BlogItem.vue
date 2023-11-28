<template>
    <div class="blog-item">
      <img src="../assets/logo_small.svg" class="item-image" alt="kleines Natamara-Logo">
      <div class="blog-item-text">
        <a :href="link"><h2 style="font-weight: 500;" class="item-name"> » {{ name }}</h2></a>
        <p class="item-description">{{ description }}</p>
      </div>
    </div>
  </template>
  
  <script>
    export default {
        props: {
            name: String,
            description: String,
            imageUrl: String,
            link: String
        }
    }
  </script>
  
  <style scoped>
  .blog-item {
    border: 0;
    border-radius: 12px;
    padding: 16px;
    text-align: left;
    background-color: #ece7ca;
    box-shadow: 0 0 6px #c9c29f;
    display: flex;
  }

  .blog-item-text {
    padding-left: 16px;
  }
  
  .item-image {
    height: auto;
    width: 10rem;
  }
  
  .item-name {
    font-size: 1.5rem;
    margin: 8px 0;
  }
  
  .item-description {
    text-align: left;
    float: left;
  }

  </style>
  