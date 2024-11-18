<template>

  <section class="container">

    <div class="section-grid">
      
      <div class="title">
        <h1> Desserts </h1>
      </div>
  
      <ProductCard />
  
    </div>
  
  </section>

</template>

<script>
import ProductCard from './components/ProductCard.vue';

export default {
  components: {
    ProductCard,
  }
}  
</script>

<style>

  .container {
    font-family: 'Red Hat Text';
    margin-top: 1%;    
    margin-left: 8%;
    margin-right: 8%;
    margin-bottom: 2%;
  }

  .section-grid {
    margin: 5%;    
    border-radius: 10px;
    padding: 3rem;
    box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;
    display: grid;
    grid-template-columns: repeat(3, auto) ;
    grid-template-rows: repeat(4, auto);
    gap:  1rem;
  }

  .section-grid>* {
    display: grid;
    justify-content: center;
    align-items: center;
  }

  .title {
    grid-column: 1 / -1;
    justify-content: start;
  }

</style>
