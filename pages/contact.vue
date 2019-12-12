<template>
  <b-container>
    <h2>Feel free to contact me</h2>
    <b-list-group flush>
      <b-list-group-item
        target="_blank"
        href="https://www.linkedin.com/in/rodolfo-dutra/"
        class="group-item"
      >
        <fa
          :icon="['fab', 'linkedin-in']"
          style="font-size: 30px"
          class="mx-2"
        />rodolfo-dutra
      </b-list-group-item>
      <b-list-group-item
        target="_blank"
        href="https://github.com/deer-rodolfo"
        class="group-item"
      >
        <fa
          :icon="['fab', 'github']"
          style="font-size: 30px"
          class="mx-2"
        />deer-rodolfo
      </b-list-group-item>
      <b-list-group-item button class="group-item">
        <fa
          :icon="['fas', 'envelope']"
          style="font-size: 30px"
          class="group-item mx-2"
        />rodolfo.borges.dutra@gmail.com
      </b-list-group-item>
    </b-list-group>
  </b-container>
</template>

<script>
export default {
  name: 'Contact'
}
</script>

<style scoped>
.group-item {
  background-color: #fdfdfd;
}
</style>
