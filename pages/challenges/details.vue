<template>
  <div>
    <!-- banner -->
    <b-row>
      <b-col cols="12" md="8" offset-md="2">
        <challenge-details
          :challenge="challenge"
          :participants="participants"
          :liked="liked"
        />
      </b-col>
    </b-row>
  </div>
</template>

<script>
import ChallengeDetails from '~/components/challenges/ChallengeDetails.vue'

export default {
  layout: 'default',
  components: {
    ChallengeDetails
  },
  data () {
    return {
      challenge: {},
      liked: false
    }
  },
  created () {
    // @TODO get and set challenge, and user preference (-> liked)
    this.challenge = {
      id: 1,
      title: '1h Yoga',
      description: 'Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.'
    }
  }
}
</script>
