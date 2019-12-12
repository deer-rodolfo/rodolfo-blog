<template>
  <div>
    <h2>A bit about myself:</h2>
    <b-row>
      <b-col sm="5" order="2" order-sm="1">
        <b-img
          src="~/assets/profile-rodolfo.jpg"
          fluid
          thumbnail
          center
          alt="Rodolfo in Lisbon"
          class="mb-3"
        ></b-img>
      </b-col>
      <b-col order="1" order-sm="2">
        <p>
          Olá! My name is Rodolfo, I am Portuguese and I was born in a small
          island named Pico, in the middle of the Atlantic. I currently live in
          Leipzig, Germany.
        </p>
        <p>
          My first passion in tech was aircrafts however, destiny brought me to
          work in web development. I am passionate about it since it makes
          bringing ideas to life easier and with fewer costs.
        </p>
        <p>
          I love reading José Saramago, I am caught up listening to Jacob
          Collier and every day I believe more in the power of our inner energy.
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
