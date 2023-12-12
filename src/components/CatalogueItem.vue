<template>
    <div class="shop-item">
      <div class="item-image-div">
        <img :src=imageUrl class="item-image">
      </div>
      <div class="name-row">
        <h2 class="item-name">{{ name }}</h2>
        <p class="item-description">{{ setupDescription }}</p>
      </div>
      <h2 class="item-price">{{ price }}</h2>
      <div v-if="imageUrls.length !== 1" class="button-wrapper">
        <div v-for="image in imageUrls" class="item-button-list">
          <button @click="switchBttn(image)" :style="setupStyle(image)" class="item-button"></button>
        </div>
      </div>
    </div>
  </template>
  
  <script>
    export default {
      data() {
    return {
      imageIndex: 0,
    };},
        
        props: {
            name: String,
            price: String,
            imageUrls: {
              type: Array,
              require: true
            },
            colors: {
              type: Array,
              require: true
            },
            descriptions: {
              type: Array,
              require: true
            }
        },
        methods: {
          switchBttn(item) {
            this.imageIndex = this.imageUrls.indexOf(item)
        },
        setupStyle(image) {
            let i = this.imageUrls.indexOf(image);
            return "background-color:" + this.colors[i];
            
          },
        
        
        },
        computed: { 
          imageUrl() {
            return this.imageUrls[this.imageIndex];
          },
          setupDescription() {
            return this.descriptions[this.imageIndex];
          }
          
          
          },
        created() {
        
        },

        mounted() {
          let urls = this.imageUrls;
          
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
  
  .item-image-div {
    width: 20rem;
    height: 20rem;
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 12px;
  }

  .item-image {
    max-width: 100%;
    border-radius: 12px;
  }
  
  .name-row {
    display: flex;
    justify-content: space-between;
  }
  .item-name {
    font-size: 1.5rem;
    margin: 8px 0;
  }

  .button-wrapper {
    display: flex;
  }

  .item-button {
    display:block;
    height: 50px;
    width: 50px;
    border-radius: 50%;
    border: 2px solid grey;
    margin-left: 8px;
    cursor: pointer;
  }
  
  .item-description {
    text-align: center;
    margin: 20px 5px 8px 0;
    float: right;
  }

  .item-price {
    float: right;
    font-weight: bold;
  }
  </style>
  