<template>
  <div>
    <b-navbar toggleable="lg" type="light" variant="light">
      <b-navbar-brand href="#">
        <b-img src="/img/logo.png" width="60" />
      </b-navbar-brand>

      <b-navbar-toggle target="nav-collapse" />

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item href="#">
            <nuxt-link to="/">
              Home
            </nuxt-link>
          </b-nav-item>
          <b-nav-item href="#">
            <nuxt-link to="/challenges">
              Challenge erstellen
            </nuxt-link>
          </b-nav-item>
          <b-nav-item href="#">
            <nuxt-link to="/challenges">
              Challenge finden
            </nuxt-link>
          </b-nav-item>
          <b-nav-item href="#">
            <nuxt-link to="/challenges">
              Meine Challenges
            </nuxt-link>
          </b-nav-item>
        </b-navbar-nav>

        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <nuxt-link class="btn-primary--outline mr-3" to="/login">
            Login
          </nuxt-link>
          <nuxt-link to="/sign-up" class="btn-secondary--outline">
            Registrieren
          </nuxt-link>
          </nuxt-link>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script></script>

<style lang="scss" scoped>
nav{
  box-shadow: 4px 4px 10px rgba(0, 0, 0, 0.25);
}
</style>
