<template>
  <div class="page-index">
    <div class="container">
      <h1 v-for="post in posts">
        {{ post.name }}
      </h1>
    </div>
  </div>
</template>

<script>
import blogPosts from '~/contents/blog.js'

export default {
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
  transition: {
    name: 'slide-fade'
  },
  head() {
    return {
      title: 'title',
      meta: [
        { name: 'author', content: 'rodolfo' },
        {
          name: 'description',
          property: 'og:description',
          content: 'hallooo',
          hid: 'description'
        }
      ]
    }
  }
}
</script>
