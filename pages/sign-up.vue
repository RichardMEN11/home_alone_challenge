<template>
  <div class="container-fluid">
    <div class="row">
      <div class="d-none d-lg-block col-lg-6">
        <h1>Never home alone again</h1>
        <p>Lorem ipsum...</p>
      </div>
      <div class="col-12 col-lg-6">
        <h1>Registrierung</h1>
        <sign-up-form />
      </div>
    </div>
  </div>
</template>

<script>
import SignUpForm from '~/components/authentification/SignUpForm.vue'

export default {
  layout: 'authentication',
  components: {
    SignUpForm
  }
}
</script>
