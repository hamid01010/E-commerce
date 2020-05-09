<template>
  <div>  
    <div class="card" style="width: 18rem;">
        <img :src="post.url" class="card-img-top">
        <div class="card-body">
            <h5 class="card-title">{{post.title}}</h5>
        </div>
    </div>

  </div>
</template>

<script>
export default {
    name: "Post",
    props: ["post"]
}
</script>

<style>

</style>