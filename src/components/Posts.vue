<template>
  <div>
      <div v-for="post in posts" :key="post.id">
          <post :post="post"/>
      </div>
  </div>
</template>

<script>
import Post from "./post"
export default {
    name: "Posts",
    props: ["posts"],
    components:{
        Post
    }
}
</script>

<style>

</style>