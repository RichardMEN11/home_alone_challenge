<template>
  <div class="card">
    <div class="card-header d-flex justify-content-between">
      <h1>{{ challenge.title }}</h1>
      <b-button type="button" @click="toggleLike">
        <font-awesome-icon :icon="likeIcon" />
      </b-button>
    </div>
    <b-card-text>
      <h2>Beschreibung:</h2>
      {{ challenge.description }}
    </b-card-text>
    <div class="card-footer">
      <h2>Teilnehmer ({{ participants.length }})</h2>
      <participants-list :participants="participants"/>
      <div class="call-to-action">
        <b-button variant="primary">
          Teilnehmen
        </b-button>
      </div>
    </div>
  </div>
</template>

<script>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
import ParticipantsList from '~/components/challenges/ParticipantsList.vue'

export default {
  components: {
    FontAwesomeIcon,
    ParticipantsList
  },
  props: {
    challenge: { type: Object, required: true },
    participants: { type: Array, default: () => { return [] } },
    liked: { type: Boolean, default: false }
  },
  computed: {
    likeIcon () {
      return this.liked === true ? ['fas', 'heart'] : ['far', 'heart']
    }
  },
  methods: {
    toggleLike () {
      // @TODO
    }
  }

}
</script>

<style scoped>
  .call-to-action {
    margin-top: 1em;
    text-align: center;
  }
</style>
