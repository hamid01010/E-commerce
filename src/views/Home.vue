<template>
  <div class="home container">
      <posts :posts="posts" />
  </div>
</template>

<script>
import axios from "axios"
import Posts from "../components/Posts"
export default {
  name: 'Home',
  components: {
    Posts
  },
  data(){
      return{
          posts:[]
      }
  },
    created(){
        axios.get("https://jsonplaceholder.typicode.com/photos?_limit=5")
        .then(res => this.posts = res.data)
        .catch(err => console.log(err))
    },
    methods:{

    }  
}
</script>
