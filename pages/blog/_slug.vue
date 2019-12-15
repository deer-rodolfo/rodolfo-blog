<template>
  <div>
    <h1>{{ attributes.title }}</h1>
    <h5 class="mb-4 secondary-text">{{ attributes.date }}</h5>
    <b-row class="mb-4">
      <b-col sm="4">
        <b-img
          :src="imageRequired"
          :alt="attributes.title"
          fluid
          center
          width="200px"
        ></b-img>
      </b-col>
      <b-col sm="8" align-self="center">
        <h5>
          <em>{{ attributes.description }}</em>
        </h5>
      </b-col>
    </b-row>
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
  computed: {
    imageRequired() {
      return require(`~/assets/images/${this.attributes.image}`)
    }
  },
  created() {
    const file = require(`~/contents/blog/${this.$route.params.slug}.md`)
    this.attributes = file.attributes
    this.dynamicComponent = file.vue.component
  }
}
</script>
