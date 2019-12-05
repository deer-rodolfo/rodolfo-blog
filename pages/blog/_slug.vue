<template>
  <div>
    <h1>{{ attributes.title }}</h1>
    <!-- eslint-disable-next-line vue/require-component-is -->
    <component :is="dynamicComponent" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      attributes: null,
      dynamicComponent: null
    }
  },
  created() {
    const file = require(`~/contents/blog/${this.$route.params.slug}.md`)
    this.attributes = file.attributes
    this.dynamicComponent = file.vue.component
  }
}
</script>
