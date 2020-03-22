<template>
  <div class="page challenge-details">
    <div class="banner" :style="challengeStyle" />
    <div class="container">
      <b-row>
        <b-col cols="12" md="8" offset-md="2">
          <challenge-details
            :challenge="challenge"
            :liked="liked"
          />
        </b-col>
      </b-row>
    </div>
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
  computed: {
    bannerImgUrl () {
      if (typeof this.challenge.img === 'string') {
        return this.challenge.img
      }
      return '/img/default-challenge-banner.png'
    },
    challengeStyle () {
      return {
        'background-image': 'url(' + this.bannerImgUrl + ')'
      }
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

<style lang="scss" scoped>

@import '../../assets/style/variables';

.page.challenge-details {
  position: relative;
  width: 100%;
  height: 100%;
  padding-top: 25vh;

  .banner {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 50vh;
    background-position: bottom;
    background-size: cover;
    background-attachment: fixed;
  }
}

</style>
