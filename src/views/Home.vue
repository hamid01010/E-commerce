<template>
  <div class="home container">
      <posts :posts="posts" />
  </div>
</template>

<script>
import Posts from "../components/Posts"
export default {
  name: 'Home',
  components: {
    Posts
  },
  data(){
      return{
          posts:[
              {
                  id: 1,
                  image: "https://images.pexels.com/photos/4142982/pexels-photo-4142982.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500",
                  title: "Cactus",
                  description: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quidem est, numquam, suscipit sequi incidunt nisi magnam ad laudantium distinctio asperiores ratione non id exercitationem nemo eum error obcaecati illum ea.",
                  completed: true
              },
              {
                  id: 2,
                  image: "https://images.pexels.com/photos/3290068/pexels-photo-3290068.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500",
                  title: "Pyramid",
                  description: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quidem est, numquam, suscipit sequi incidunt nisi magnam ad laudantium distinctio asperiores ratione non id exercitationem nemo eum error obcaecati illum ea.",
                  completed: false
              }
          ]
      }
  }
}
</script>
