<template>
  <div class="d-flex flex-wrap">
    <avatar
      v-for="user of participants"
      :key="'participant-' + user.username"
      :src="user.avatar"
      :title="user.username"
    />
    <b-button
      v-if="hasMoreParticipants"
      variant="link"
      size="lg"
      @click="loadMore"
    >
      ...
    </b-button>
  </div>
</template>

<script>

import Avatar from '~/components/user/Avatar.vue'

export default {
  components: {
    Avatar
  },
  props: {
    participants: { type: Array, default: () => { return [] } },
    total: { type: Number, default: 0 }
  },
  computed: {
    hasMoreParticipants () {
      return this.participants.length < this.total
    }
  },
  methods: {
    toggleLike () {
      // @TODO
    },
    loadMore () {
      this.$emit('load-more')
    }
  }
}
</script>

<style scoped>
  .avatar {
    margin: 0.1em;
  }
</style>
