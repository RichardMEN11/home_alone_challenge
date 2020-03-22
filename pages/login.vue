<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-12 col-md-6 authentification--hero">
        <div>
          <h1>Never home<br/>alone <span class="text-primary">again</span></h1>
        </div>
      </div>
      <div class="col-12 col-md-6 col-lg-4 offset-lg-1">
        <div class="card">
          <div class="card-body">
            <h2>Login</h2>
            <login-form />
          </div>
        </div>
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
