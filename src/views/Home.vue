<template>
  <div class="container">
      <products :products="products"/>
  </div>
</template>

<script>
import axios from "axios"
import Products from "../components/Products" 
export default {
    name: "Home",
    components:{
        Products
    },
    created(){
        axios.get("https://jsonplaceholder.typicode.com/photos?_limit=5")
        .then(res => this.products = res.data)
        .catch(err => console.log(err))
    },
    data(){
        return{
            products:[]
        }
    }
}
</script>

<style>

</style>