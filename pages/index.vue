<template>
  <div>
    <b-container class="index--hero" fluid>
      <b-row class="h-100  align-items-center">
        <b-col sm="0" md="2" />
        <b-col md="8" sm="12" class="justify-content-center">
          <h1 class="index--hero-heading">
            Du suchst grade nach neuen <span class="highlighted">Aufgaben?</span>
          </h1>
          <p class="index--hero-subheading">
            Dann melde dich an und mach bei XXX mit...
          </p>

          <nuxt-link class="btn-primary mt-1" to="/sign-up">
            Anmelden
          </nuxt-link>
          <br class="d-md-none">
          <nuxt-link class="btn-primary ml-md-4 mt-1" to="/login">
            Challenge finden
          </nuxt-link>
        </b-col>
        <b-col sm="0" md="2" />
      </b-row>
    </b-container>
    <b-container class="my-5">
      <b-row>
        <b-col md="4" order-sm="1" order-md="1">
          <b-img src="/img/blob1.png" fluid alt="Responsive image" />
        </b-col>
        <b-col md="7" offset-md="1" order-md="2">
          <h2 class="mt-5 py-auto">
            Erstelle eine <span class="highlighted">Challenge</span>
          </h2>
          <p class="index--paragraph pt-4">
            Ipsum elit magna est sunt amet. Qui aute culpa irure cillum adipisicing minim ad dolore cillum id commodo occaecat adipisicing. Sit tempor ad nostrud est fugiat aliquip do enim sit culpa voluptate officia. Pariatur ullamco cillum laborum adipisicing nulla laboris amet do. Aliqua quis sunt duis ut eu magna ex aliqua nostrud aliquip sint duis elit. Sunt anim culpa ad irure minim non fugiat cillum mollit pariatur ipsum irure.
          </p>
        </b-col>
      </b-row>
    </b-container>
    <b-container class="my-5">
      <b-row>
        <b-col md="7" order-sm="1" order-md="2">
          <h2 class="mt-5 py-auto">
            Verwende deine Zeit  <span class="highlighted">sinnvoll</span>
          </h2>
          <p class="index--paragraph pt-4">
            Ipsum elit magna est sunt amet. Qui aute culpa irure cillum adipisicing minim ad dolore cillum id commodo occaecat adipisicing. Sit tempor ad nostrud est fugiat aliquip do enim sit culpa voluptate officia. Pariatur ullamco cillum laborum adipisicing nulla laboris amet do. Aliqua quis sunt duis ut eu magna ex aliqua nostrud aliquip sint duis elit. Sunt anim culpa ad irure minim non fugiat cillum mollit pariatur ipsum irure.
          </p>
        </b-col>
        <b-col md="4" offset-md="1" order-sm="1" order-md="2">
          <b-img src="/img/blob2.png" fluid alt="Responsive image" />
        </b-col>
      </b-row>
    </b-container>
    <b-container class="my-5">
      <b-row>
        <b-col md="4">
          <b-img src="/img/blob3.png" fluid alt="Responsive image" class="mt-5" />
        </b-col>
        <b-col md="7" offset-md="1">
          <h2 class="mt-5 py-auto">
            So  <span class="highlighted">funktionierts</span>
          </h2>
          <b-row class="mt-5">
            <b-col md="2" class="text-center">
              <h3 class="index--number">
                01
              </h3>
            </b-col>
            <b-col>
              <h5><span class="highlighted">Anmelden auf XXX</span></h5>
              <p>Lorem reprehenderit eiusmod tempor laborum deserunt officia velit. Magna aute id incididunt dolore incididunt non aute minim. Lorem nulla enim est consectetur..</p>
            </b-col>
          </b-row>
          <b-row>
            <b-col md="2" class="text-center">
              <h3 class="index--number">
                02
              </h3>
            </b-col>
            <b-col>
              <h5><span class="highlighted">Challenge finden</span></h5>
              <p>Lorem reprehenderit eiusmod tempor laborum deserunt officia velit. Magna aute id incididunt dolore incididunt non aute minim. Lorem nulla enim est consectetur..</p>
            </b-col>
          </b-row>
          <b-row>
            <b-col md="2" class="text-center">
              <h3 class="index--number">
                03
              </h3>
            </b-col>
            <b-col>
              <h5><span class="highlighted">Challenge umsetzen</span></h5>
              <p>Lorem reprehenderit eiusmod tempor laborum deserunt officia velit. Magna aute id incididunt dolore incididunt non aute minim. Lorem nulla enim est consectetur..</p>
            </b-col>
          </b-row>
        </b-col>
        <b-col />
      </b-row>
    </b-container>
    <b-container class="my-5">
      <b-row>
        <b-col md="7" order-sm="1" order-md="2">
          <h2 class="mt-5 py-auto">
            Meld dich an <span class="highlighted">mach mit!</span>
          </h2>
          <p class="index--paragraph pt-4">
            Ipsum elit magna est sunt amet. Qui aute culpa irure cillum adipisicing minim ad dolore cillum id commodo occaecat adipisicing. Sit tempor ad nostrud est fugiat aliquip do enim sit culpa voluptate officia. Pariatur ullamco cillum laborum adipisicing nulla laboris amet do. Aliqua quis sunt duis ut eu magna ex aliqua nostrud aliquip sint duis elit. Sunt anim culpa ad irure minim non fugiat cillum mollit pariatur ipsum irure.
          </p>
        </b-col>
        <b-col md="4" offset-md="1" order-sm="1" order-md="2">
          <b-img src="/img/blob2.png" fluid alt="Responsive image" />
        </b-col>
      </b-row>
    </b-container>
    <b-container class="text-center h-100 index--last" fluid>
      <div class="b-row index--button-end mt-5 pt-5">
        <nuxt-link to="/sign-up" class="btn-primary">
          Anmelden
        </nuxt-link>
        <nuxt-link class="btn-primary ml-4" to="/login">
          Challenge finden
        </nuxt-link>
      </div>
    </b-container>
  </div>
</template>

<script>

export default {
  components: {

  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/variables';

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
    &--paragraph{
      font-size: 18px;
      line-height: 30px;
    }
    &--number{
      color: white;
      background-color: $secondary;
      border-radius: 7px;
      margin: 20px 0;
    }
    &--button-end{
      height: 40vh;
    }
    &--last{
      background-image: url('/img/background.png');
      background-size: contain;
      background-position: bottom;
      background-repeat: no-repeat;
      display: flex;
      justify-content: center;
      align-items: center;
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
