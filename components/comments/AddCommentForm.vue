<template>
  <div class="add-comment-form">
    <b-form @submit="onSubmit">
      <avatar :src="currentUser.avatar" :title="currentUser.username" />

      <b-form-group label-for="add-comment-message">
        <b-form-input
          id="add-comment-message"
          v-model="message"
          type="text"
          required
          placeholder="Berichte über deine Challenge ..."
        ></b-form-input>
      </b-form-group>

      <b-button type="submit" variant="secondary">
        <font-awesome-icon icon="paper-plane" />
      </b-button>
    </b-form>

    <div class="bg-danger" v-if="errors">
      {{ errors }}
    </div>
  </div>
</template>

<script>

import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
import Avatar from '~/components/user/Avatar.vue'

export default {
  components: {
    Avatar,
    FontAwesomeIcon
  },
  data () {
    return {
      errors: null,
      message: null
    }
  },
  computed: {
    currentUser () {
      // @TODO get current user from user Vuex store
      return {}
    }
  },
  methods: {
    onSubmit () {
      this.resetErrors()
      this.addComment()
    },
    resetErrors () {
      this.errors = null
    },
    async addComment () {
      const data = {}
      data.message = this.message
      data.user_id = this.currentUser.id
      data.challenge_id = this.challenge_id
      try {
        await this.$store.dispatch('login', data)
      } catch (e) {
        // @TODO specify error message
        this.errors = 'Ein Fehler ist aufgetreten.'
      }
    }
  }
}
</script>

<style lang="scss">
@import '../../assets/style/variables';

  .add-comment-form {
    margin: 2em 0 1em 0;
    form {
      display: grid;
      grid-template-columns: 4em auto 4em;

      button[type="submit"] {
        padding: 0;
        width: 2.5em;
        height: 2.5em;
        margin-left: 0.5em;
        padding: 0;
      }
    }
  }
</style>
