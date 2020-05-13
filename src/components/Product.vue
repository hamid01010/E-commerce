<template>
  <div>
        <div class="card">
            <img class="card-img-top" :src="product.url" alt="Card image cap">
            <div class="card-body">
                <router-link :to="{name: 'productPage', params: {id: product.id} }"><h5 class="card-title">{{product.title}}</h5></router-link>
            </div>
        </div>
  </div>
</template>

<script>
export default {
    name: "Product",
    props: ["product"]
}
</script>

<style>

</style>