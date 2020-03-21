<template>
  <div>
    <b-navbar toggleable="lg" type="light" variant="light">
      <b-navbar-brand href="#">
        HomeAlone
      </b-navbar-brand>

      <b-navbar-toggle target="nav-collapse" />

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item href="#">
            Home
          </b-nav-item>
          <b-nav-item href="#">
            Challenge erstellen
          </b-nav-item>
          <b-nav-item href="#">
            Challenge finden
          </b-nav-item>
        </b-navbar-nav>

        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-button variant="outline-primary mr-3">
            Login
          </b-button>
          <b-button variant="outline-primary">
            Registrieren
          </b-button>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script></script>

<style lang="scss" scoped></style>
