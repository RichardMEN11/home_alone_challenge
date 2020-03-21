<template>
  <div class="container-fluid">
    <div class="row">
      <div class="d-none d-lg-block col-lg-6">
        <h1>Never home alone again</h1>
        <p>Lorem ipsum...</p>
      </div>
      <div class="col-12 col-lg-6">
        <h1>Login</h1>
        <login-form />
      </div>
    </div>
  </div>
</template>

<script>
import LoginForm from '~/components/authentification/LoginForm.vue'

export default {
  layout: 'authentication',
  components: {
    LoginForm
  }
}
</script>
