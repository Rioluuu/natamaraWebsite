<template>
    <div class="shop-item">
      <h2 class="item-name">{{ name }}</h2>
      <div v-if="descriptions != null">
        <h3>Sorte: <u>{{ setupDescription }}</u></h3>
      </div>
      {{ setupIngredients }}
      <div v-if="imageUrls.length !== 1" class="button-wrapper">
        <div v-for="image in imageUrls">
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
              require: false
            },
            ingredients: {
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
          setupIngredients() {
            return this.ingredients[this.imageIndex];
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
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .item-name {
    font-size: 1.5rem;
    margin: 8px 0;
  }

  .button-wrapper {
    display: flex;
    justify-content: center;
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
  </style>
  