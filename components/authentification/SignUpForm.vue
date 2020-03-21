<template>
  <div>
    <b-form @submit="onSubmit">
      <b-form-group label="Benutzername" label-for="sign-up-username">
        <b-form-input
          id="sign-up-username"
          v-model="form.username"
          type="text"
          required
          placeholder="Benutzername"
        ></b-form-input>
      </b-form-group>

      <b-form-group label="E-Mail" label-for="sign-up-email">
        <b-form-input
          id="sign-up-email"
          v-model="form.email"
          type="email"
          required
          placeholder="E-Mail"
        ></b-form-input>
      </b-form-group>

      <b-form-group label="Passwort" label-for="sign-up-password">
        <b-form-input
          id="sign-up-password"
          v-model="form.password"
          type="password"
          required
          placeholder="Passwort"
        ></b-form-input>
      </b-form-group>

      <b-form-group label="Passwort wiederholen" label-for="sign-up-password-repeat">
        <b-form-input
          id="sign-up-password-repeat"
          v-model="form.passwordrepeat"
          type="passwordrepeat"
          required
          placeholder="Passwort wiederholen"
        ></b-form-input>
      </b-form-group>

      <div class="d-flex justify-content-between">
        <b-button type="submit" variant="primary">Registrieren</b-button>
        <b-button type="button" href="/" variant="secondary">Zurück</b-button>
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
      this.signUp()
    },
    resetErrors () {
      this.errors = null
    },
    async signUp () {
      try {
        await this.$store.dispatch('sign-up', this.form)
      } catch (e) {
        // @TODO specify error message
        this.errors = 'Ein Fehler ist aufgetreten.'
      }
    }
  }
}
</script>
