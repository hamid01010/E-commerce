<template>
  <div>
        <div class="card">
            <img class="card-img-top" :src="product.url" alt="Card image cap">
            <div class="card-body">
                <h5 class="card-title">{{product.title}}</h5>
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