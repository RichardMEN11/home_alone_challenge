<template>
  <div>
    <b-form @submit="onSubmit">
      <b-form-group label="E-Mail" label-for="login-email">
        <b-form-input
          id="login-email"
          v-model="form.email"
          type="email"
          required
          placeholder="E-Mail"
        ></b-form-input>
      </b-form-group>

      <b-form-group label="Passwort" label-for="login-password">
        <b-form-input
          id="login-password"
          v-model="form.name"
          type="password"
          required
          placeholder="Passwort"
        ></b-form-input>
      </b-form-group>

      <div class="text-left">
        <b-link href="#forgot-password">Passwort vergessen?</b-link>
      </div>

      <div class="bg-danger" v-if="errors">
        {{ errors }}
      </div>

      <b-button type="submit" variant="primary">Login</b-button>

      <div class="text-left">
        Noch nicht registriert?
        <b-link href="/register">Klicke hier.</b-link>
      </div>
    </b-form>
  </div>
</template>

<script>
export default {
  data () {
    return {
      errors: null,
      form: {}
    }
  },
  methods: {
    onSubmit () {
      this.resetErrors()
      this.login()
    },
    resetErrors () {
      this.errors = null
    },
    async signUp () {
      try {
        await this.$store.dispatch('login', this.form)
      } catch (e) {
        // @TODO specify error message
        this.errors = 'Ein Fehler ist aufgetreten.'
      }
    }
  }
}
</script>
