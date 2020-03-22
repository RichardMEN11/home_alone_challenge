<template>
  <div class="card">
    <div class="card-header d-flex justify-content-between">
      <h1>{{ challenge.title }}</h1>
      <b-button type="button" :variant="liked ? 'primary' : 'secondary'" class="like" @click="toggleLike">
        <font-awesome-icon :icon="likeIcon" />
      </b-button>
    </div>
    <b-card-text>
      <h2>Beschreibung:</h2>
      {{ challenge.description }}
    </b-card-text>
    <div class="card-footer">
      <h2>Teilnehmer ({{ participants.length }})</h2>
      <participants-list
        :participants="participants"
        @load-more="loadMoreParticipants"
      />
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
    liked: { type: Boolean, default: false }
  },
  data () {
    return {
      participants: []
    }
  },
  computed: {
    likeIcon () {
      return this.liked === true ? ['fas', 'heart'] : ['far', 'heart']
    }
  },
  created () {
    this.fetchParticipants(0, 10)
  },
  methods: {
    toggleLike () {
      // @TODO
    },
    loadMoreParticipants () {
      // @TODO use offset and limit
      this.fetchParticipants()
    },
    async fetchParticipants (offset, limit) {
      const data = { challenge_id: this.challenge_id }
      if (Number.isInteger(offset)) {
        data.offset = offset
      }
      if (Number.isInteger(limit)) {
        data.limit = limit
      }
      try {
        await this.$store.dispatch('load-more-participants', data)
      } catch (e) {
        // @TODO specify error message
        this.errors = 'Ein Fehler ist aufgetreten.'
      }
    }
  }

}
</script>

<style lang="scss" scoped>

@import '../../assets/style/variables';

.page.challenge-details {
  padding-top: 25vh;
  background-position: bottom;
  background-size: cover;
  height: 50vh;
  background-attachment: fixed;
  h1, h2 {
    color: $primary;
  }
  .card-header,
  .card-footer {
    background-color: inherit;
    border: none;
  }
  .card-text {
    padding: 0.75rem 1.25rem;
  }
  .call-to-action {
    margin-top: 1em;
    text-align: center;
  }
  button.like {
    height: 2em;
    width: 2em;
    font-size: 1.5em;
    text-align: center;
    padding: 0;
  }
}

</style>
