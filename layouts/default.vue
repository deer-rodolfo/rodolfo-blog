<template>
  <div>
    <b-container class="container">
      <b-navbar toggleable="lg" class="mt-5">
        <nuxt-link :to="{ name: 'index' }">
          <b-navbar-brand class="nav-title">
            Rodolfo Dutra
            <p class="nav-subtitle secondary-text ml-4">Curious Developer</p>
          </b-navbar-brand>
        </nuxt-link>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav class="ml-auto">
            <b-nav-item class="nav-item">
              <nuxt-link :to="{ name: 'about' }">
                About
              </nuxt-link>
            </b-nav-item>
            <b-nav-item class="nav-item">
              <nuxt-link :to="{ name: 'contact' }">
                Contact
              </nuxt-link>
            </b-nav-item>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
      <b-row align-h="center">
        <b-col lg="8" md="10" sm="12">
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
body {
  font-family: 'Baskervville', serif;
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
  color: rgba(37, 37, 37, 0.9);
}

.secondary-text {
  color: rgba(37, 37, 37, 0.7);
}
</style>
