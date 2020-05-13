<template>
<div>
    <input type="text" v-model="search" placeholder="search products">
  <div class="row">
      <div class="col-sm-4 mb-2" v-for="product in filteredProducts" :key="product.id">
          <product :product="product"/>
      </div>
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
    props: ["products"],
    computed:{
        filteredProducts(){
           return this.products.filter((product) =>{
               return product.title.match(this.search)
           })
        }
    },
    data(){
        return{
            search: ""
        }
    }
}
</script>

<style>

</style>