<template>
  <div class="sidebar">
    <ul>
      <li v-for="post in posts" :key="post.id">
        {{post.title}}
      </li>
    </ul>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  name: 'BlogHome',
  created() {
    const uri = 'https://jsonplaceholder.typicode.com/posts/'
    axios.get(uri).then(res => {
      console.log(res.data)
      this.posts = res.data
    })
  },
  data: () => ({
    posts: []
  })
}
</script>
