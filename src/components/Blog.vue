<template>
  <div>
    <h1>{{ post.title }}</h1>
    <p>
      {{ post.body }}
    </p>
  </div>
</template>

<script>
export default {
  name: 'Blog',
  props: ['posts'],
  computed: {
    blogId() {
      return this.$route.params.id
    },
    post() {
      return this.posts.find(t => String(t.id) === this.blogId)
    }
  }
}
</script>
