<template>
  <div>
    <h1>Products page</h1>
    <div class="products">
      <article v-for="product in products.products">
        <div class="art-image">
          <img :src="product.thumbnail" alt="">
        </div>
        <p>{{product.title}}</p>
      </article>
    </div>
  </div>
</template>

<script setup>
  const { data: products } = await useFetch('https://dummyjson.com/products', {});
</script>

<style>
  .products{
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
  }
  .products article{
    width: 32%;
    margin: 15px 0;
  }
  .products article .art-image{
    height: 255px;
    position: relative;
    overflow: hidden;
  }
  .products article .art-image img{
    object-fit: fill;
  }
</style>