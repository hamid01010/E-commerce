<template>
  <div class="row">
      <div class="col-sm-4 mb-2" v-for="product in products" :key="product.id">
          <product :product="product"/>
      </div>
  </div>
</template>

<script>
import Product from "./Product"
export default {
    name: "Products",
    components:{
        Product
    },
    props: ["products"]
}
</script>

<style>

</style>