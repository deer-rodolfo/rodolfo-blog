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
      <b-row>
        <b-col sm="4">
          <b-img
            :src="imageRequired"
            :alt="post.title"
            fluid
            center
            width="200px"
          ></b-img>
        </b-col>
        <b-col sm="8">
          <b-card-text class="mt-3">
            {{ post.description }}
          </b-card-text>
        </b-col>
      </b-row>
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
  },
  computed: {
    imageRequired() {
      return require(`~/assets/images/${this.post.image}`)
    }
  }
}
</script>

<style scoped>
.blog-card {
  background-color: #fdfdfd;
  border: none;
}
</style>
