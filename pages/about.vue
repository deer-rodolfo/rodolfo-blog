<template>
  <div>
    <h2>A bit about myself:</h2>
    <b-row>
      <b-col sm="5" order="2" order-sm="1">
        <b-img
          src="~/assets/profile-rodolfo.jpg"
          fluid
          thumbnail
          alt="Rodolfo in Lisbon"
          class="mb-3"
        ></b-img>
      </b-col>
      <b-col order="1" order-sm="2">
        <p>
          Hi! My name is Rodolfo, I am Portuguese and I was born in a small
          island named Pico, in the middle of the Atlantic. I currently live in
          Leipzig, Germany.
        </p>
        <p>
          I feel passionate about using simplicity and practicality as tools to
          solve problems and bring ideas to life. That is at least what I try to
          achieve through projects and dedicated learning.
        </p>
        <p>
          My first passion in tech was airplanes, however destiny brought me to
          a path where I work in web-development and keep gaining interest in
          data-science.
        </p>
        <p>
          I love reading José Saramago, I am caught up listening to Jacob
          Collier and everyday I believe more in the power of our inner energy.
        </p>
      </b-col>
    </b-row>
  </div>
</template>

<script>
export default {
  name: 'About'
}
</script>

<style></style>
