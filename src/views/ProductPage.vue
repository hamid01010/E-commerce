<template>
    <div class="productPage">
        <img :src="product.url">
        <br>
        {{ product.title }}
    </div>
</template>

<script>
import axios from 'axios'

export default {
    name: 'product-page',
    data() {
        return {
            product: {}
        }
    },
    mounted() {
        this.fetch()
    },
    methods: {
        fetch() {
             axios.get("https://jsonplaceholder.typicode.com/photos/" + this.$route.params.id)
            .then(res => this.product = res.data)
            .catch(err => console.log(err))
        }
    }
}
</script>