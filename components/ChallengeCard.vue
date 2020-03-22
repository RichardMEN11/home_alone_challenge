<template>
  <b-row>
    <b-col md="4" sm="12" class="mt-3">
      <h3><span class="highlighted">{{ categorie }}</span><br> Challenges</h3>
    </b-col>
    <b-col md="8" sm="12">
      <div class="dashboard--card-challenge">
        <b-img :src="fotoLink" fluid alt="Responsive image" class="card--img" />
        <div class="card--text">
          <h4><strong>Challenge: </strong>{{ title }}</h4>
          <p>
            {{ text }}
          </p>
          <nuxt-link class="btn-primary" to="/challenges">
            Mehr erfahren
          </nuxt-link>
        </div>
      </div>
    </b-col>
  </b-row>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: ''
    },
    text: {
      type: String,
      default: ''
    },
    categorie: {
      type: String,
      required: true
    },
    fotoLink: {
      type: String,
      default: '/img/placeholder.png'
    }

  }
}
</script>

<style lang="scss" scoped>

.dashboard{
    &--card-challenge{
        box-shadow: 4px 4px 10px rgba(0, 0, 0, 0.25);
        margin-top: 2rem;
        border-radius: 7px;

        > .card--img{
            border-radius: 7px 7px 0px 0px;;
            width: 100%;
        }
        > .card--text{
            padding: 3rem 6rem;
        }
      }
}
</style>
