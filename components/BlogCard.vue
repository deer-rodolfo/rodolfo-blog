<template>
  <nuxt-link :to="{ name: 'blog-slug', params: { slug: post.name } }">
    <b-card
      :title="post.title"
      :sub-title="post.date"
      title-tag="h2"
      sub-title-tag="h6"
      border-variant="light"
      class="blog-card my-2"
    >
      <b-card-text>
        {{ post.description }}
      </b-card-text>
    </b-card>
  </nuxt-link>
</template>

<script>
export default {
  name: 'BlogCard',
  props: {
    post: {
      type: Object,
      default: null
    }
  }
}
</script>

<style scoped>
.blog-card {
  background-color: #fdfdfd;
  border: none;
}
.blog-card:hover {
  background-color: #ffffff;
}
</style>
