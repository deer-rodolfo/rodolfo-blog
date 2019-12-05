<template>
  <div>
    <h1>{{ title }}</h1>
    <p v-html="content"></p>
  </div>
</template>

<script>
export default {
  async asyncData({ params, app }) {
    const fileContent = await import(`~/contents/blog/${params.slug}.md`)
    const attr = fileContent.attributes
    return {
      name: params.slug,
      title: attr.title,
      year: attr.year,
      content: fileContent.html
    }
  }
}
</script>
