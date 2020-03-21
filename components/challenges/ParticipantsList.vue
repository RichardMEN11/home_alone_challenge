<template>
  <div class="d-flex flex-wrap">
    <avatar
      v-for="user of visibleParticipants"
      :key="'participant-' + user.username"
      :src="user.avatar"
      :title="user.username"
    />
    <b-button
      v-if="hasManyParticipants && !showAll"
      variant="link"
      size="lg"
      @click="toggleShowAll"
    >
      <font-awesome-icon icon="caret-down"/>
    </b-button>
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
  props: {
    participants: { type: Array, default: () => { return [] } }
  },
  data () {
    return {
      showAll: false
    }
  },
  computed: {
    visibleParticipants () {
      if (this.hasManyParticipants && !this.showAll) {
        return this.participants.slice(0, 20)
      }
      return this.participants
    },
    hasManyParticipants () {
      return this.participants.length > 20
    }
  },
  methods: {
    toggleLike () {
      // @TODO
    },
    toggleShowAll () {
      this.showAll = !this.showAll
    }
  }
}
</script>

<style scoped>
  .avatar {
    margin: 0.1em;
  }
</style>
