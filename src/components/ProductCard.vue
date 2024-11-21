<template>
  <section
    v-for="(product, index) in products"
    :key="index"
  >
    <div class="cardSection">
      <img 
      :src="product.image.desktop"
      class="imgProduct"
      /> 
      <button class="buttonAddCard"> add to Card </button>
    </div>

    <span class="category"> {{ product.category }} </span>
    <h2> {{ product.name }} </h2>
    <span class="price"> R$ {{ product.price }} </span>
  </section>
</template>

<script>
  export default {
   
    data() {
      return {
        products: [],
      }
    },

    async mounted() {
      await this.fetchData();
    },

    methods: {
      async fetchData() {
        const response = await fetch('../../data.json');
        this.products = await response.json();
        console.log(this.products)
      }
    }

  }
</script>

<style>

  section {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .cardSection {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  img {
    display: flex;
    width: 100%;
  }

  .buttonAddCard {
    position: absolute;
    border-radius: 20px;
    width: 10%;
    margin-top: 21%;
    padding: 0.5rem
  }

  .category {
    margin-top: 3rem;
    font-size: 100%;
  }

  h2 {
    font-size: 100%;
  }

  .price {
    font-size: 100%;
  }
</style>
