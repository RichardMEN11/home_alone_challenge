<template>
  <b-row>
    <b-col cols="8">
      <div class="dashboard--card-challenge">
        <b-img src="/img/placeholder.jpg" fluid alt="Responsive image" class="card--img" />
        <div class="card--text">
          <h4><strong>Challenge: </strong>{{ title }}</h4>
          <p>
            {{ text }}
          </p>
          <b-button>Mehr erfahren</b-button>
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
            border-radius: 7px 7px 0px 0px;
            height: 30%;
            width: 100%;
        }
        > .card--text{
            padding: 3rem 6rem;
        }
      }
}
</style>
