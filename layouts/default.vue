<template>
  <div>
    <b-container class="container">
      <b-row align-h="center">
        <b-col lg="8" md="10" sm="12">
          <b-row class="mt-5 mb-2" align-h="between">
            <b-col cols="12" sm="6" md="6" lg="5">
              <nuxt-link :to="{ name: 'index' }">
                <h1 class="nav-title">
                  Rodolfo Dutra
                  <p class="nav-subtitle secondary-text ml-4">
                    Curious Developer
                  </p>
                </h1>
              </nuxt-link>
            </b-col>
            <b-col sm="4" md="4" class="text-right" align-self="center">
              <nuxt-link :to="{ name: 'about' }" class="nav-item"
                >About</nuxt-link
              >
              <nuxt-link
                :to="{ name: 'contact' }"
                class="nav-item px-1 text-left"
                >Contact</nuxt-link
              >
            </b-col>
          </b-row>

          <nuxt />
        </b-col>
      </b-row>
      <footer class="text-center">
        <p>© 2019 Rodolfo Dutra</p>
      </footer>
    </b-container>
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css?family=Raleway&display=swap');
body {
  font-family: 'Raleway', sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  color: #252525;
  background-color: #fdfdfd;
  margin: 0 0 30px;
}

html {
  position: relative;
  min-height: 100%;
}

footer {
  position: absolute;
  left: 0;
  bottom: 0;
  height: 40px;
  width: 100%;
}
.blog-link {
  text-decoration: underline;
}

a {
  text-decoration: none;
  color: #252525;
}
a:hover {
  text-decoration: none;
  color: #252525;
}

.nav-title {
  font-size: 2rem;
}

.nav-subtitle {
  font-size: 1.5rem;
}

.nav-item {
  font-size: 1.3rem;
  color: rgba(37, 37, 37, 0.7);
}

.secondary-text {
  color: rgba(37, 37, 37, 0.7);
}
</style>
