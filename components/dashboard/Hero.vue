<template>
  <b-container class="index--hero" fluid>
    <b-row class="h-100  align-items-center">
      <b-col sm="0" md="2" />
      <b-col md="8" sm="12" class="justify-content-center">
        <h1 class="index--hero-heading">
          {{ heading[0] }} <span class="highlighted">{{ heading[1] }}</span>
        </h1>
        <p class="index--hero-subheading">
          {{ subheading }}
        </p>

        <nuxt-link v-if="firstButtonLink" class="btn-primary mt-1" :to="firstButtonLink">
          {{ firstButtonText }}
        </nuxt-link>
        <br class="d-md-none">
        <nuxt-link v-if="secondButtonLink" class="btn-primary ml-md-4 mt-1" :to="secondButtonLink">
          {{ secondButtonText }}
        </nuxt-link>
      </b-col>
      <b-col sm="0" md="2" />
    </b-row>
  </b-container>
</template>

<script>
export default {
  props: {
    heading: {
      type: Array,
      required: true
    },
    subheading: {
      type: String,
      required: false,
      default: ''
    },
    firstButtonLink: {
      type: String,
      required: false,
      default: ''
    },
    firstButtonText: {
      type: String,
      required: false,
      default: ''
    },
    secondButtonText: {
      type: String,
      required: false,
      default: ''
    },
    secondButtonLink: {
      type: String,
      required: false,
      default: ''
    }
  }

}
</script>

<style lang="scss" scoped>
@import '../../assets/style/variables';
.index{
    &--hero{
      font-family: Helvetica;
      background-image: linear-gradient(0deg, rgba(34, 45, 65, 0.85), rgba(34, 45, 65, 0.85)), url('/img/placeholder.jpg');
      background-position:  center;
      background-size: cover;
      height: 60vh;
      &-heading{
        font-style: italic;
        font-weight: bold;
        color: white;
        font-size: 60px;
        line-height: 92px;
      }
      &-subheading{
        color: white;
        font-style: italic;
        font-weight: bold;
        font-size: 25px;
        padding: 2rem 0;
      }
    }
}
@media only screen and (max-width: 420px){
    .index{
      &--hero{
        height: 65vh;
        &-heading{
          font-size: 30px;
          line-height: 30px;
        }
        &-subheading{
          font-size: 20px;
          line-height: 25px;
        }
      }
    }
  }
</style>
