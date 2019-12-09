<template>
  <div>
    <blog-card v-for="post in posts" :key="post.id" :post="post" />
  </div>
</template>

<script>
import blogPosts from '~/contents/blog.js'
import BlogCard from '~/components/BlogCard'

export default {
  components: {
    BlogCard
  },
  asyncData({ app }) {
    async function asyncImport(blogName) {
      const wholeMD = await import(`~/contents/blog/${blogName}.md`)
      return wholeMD.attributes
    }
    return Promise.all(blogPosts.map((blog) => asyncImport(blog))).then(
      (res) => {
        return {
          posts: res
        }
      }
    )
  },
  head() {
    return {
      title: 'Rodolfo Dutra - Curious Developer',
      meta: [
        { name: 'author', content: 'deer-rodolfo' },
        {
          name: 'description',
          property: 'og:description',
          content:
            'A collection of ideas and projects. That is the idea I have for this personal blog.',
          hid: 'description'
        }
      ]
    }
  }
}
</script>
