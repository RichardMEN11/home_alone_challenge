<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-12 col-md-6 authentification--hero">
        <div>
          <h1>Never home<br/>alone <span class="text-primary">again</span></h1>
          <p>
            Registriere dich jetzt und connecte dich mit tausenden Menschen virtuell!
          </p>
        </div>
      </div>
      <div class="col-12 col-md-6 col-lg-4 offset-lg-1">
        <div class="card">
          <div class="card-body">
            <h2>Registrierung</h2>
            <sign-up-form />
          </div>
        </div>
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
