<template>
  <main class="wrapper">
    <h1>Products</h1>

    <div class="card-container">
      <ProductCardComponent class="card" v-for="product in inventory.slice(3)" :key="product.id" :product="product"
        :addToCart="addToCart" />
    </div>
  </main>

</template>

<script>
import ProductCardComponent from '@/components/ProductCardComponent.vue'

export default {
  name: 'ProductsView',
  props: ['inventory', 'addToCart'],
  components: {
    ProductCardComponent
  }
}
</script>
