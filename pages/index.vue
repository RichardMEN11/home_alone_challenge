<template>
  <div>
    <Hero
      :heading="['Du suchst grade nach neuen ', 'Aufgaben']"
      subheading="Dann melde dich an und mach bei XXX mit..."
      first-button-link="/sign-up"
      first-button-text="Anmelden"
      second-button-link="/login"
      second-button-text="Challenge finden"
    />
    <TextImageSection
      :heading="['Verwende deine Zeit', 'sinnvoll']"
      text="  Ipsum elit magna est sunt amet. Qui aute culpa irure cillum adipisicing minim ad dolore cillum id commodo occaecat adipisicing. Sit tempor ad nostrud est fugiat aliquip do enim sit culpa voluptate officia. Pariatur ullamco cillum laborum adipisicing nulla laboris amet do. Aliqua quis sunt duis ut eu magna ex aliqua nostrud aliquip sint duis elit. Sunt anim culpa ad irure minim non fugiat cillum mollit pariatur ipsum irure."
      img-link="/img/blob1.png"
    />
    <TextImageSection
      :heading="['Erstelle eine', 'Challenge']"
      text="  Ipsum elit magna est sunt amet. Qui aute culpa irure cillum adipisicing minim ad dolore cillum id commodo occaecat adipisicing. Sit tempor ad nostrud est fugiat aliquip do enim sit culpa voluptate officia. Pariatur ullamco cillum laborum adipisicing nulla laboris amet do. Aliqua quis sunt duis ut eu magna ex aliqua nostrud aliquip sint duis elit. Sunt anim culpa ad irure minim non fugiat cillum mollit pariatur ipsum irure."
      img-link="/img/blob2.png"
      img-pos="right"
    />
    <b-container class="my-5 py-5">
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
    <TextImageSection
      :heading="['Melde dich an', 'mach mit!']"
      text="  Ipsum elit magna est sunt amet. Qui aute culpa irure cillum adipisicing minim ad dolore cillum id commodo occaecat adipisicing. Sit tempor ad nostrud est fugiat aliquip do enim sit culpa voluptate officia. Pariatur ullamco cillum laborum adipisicing nulla laboris amet do. Aliqua quis sunt duis ut eu magna ex aliqua nostrud aliquip sint duis elit. Sunt anim culpa ad irure minim non fugiat cillum mollit pariatur ipsum irure."
      img-link="/img/blob4.png"
      img-pos="right"
    />
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
import Hero from '../components/dashboard/Hero'
import TextImageSection from '../components/dashboard/TextImageSection'

export default {
  components: {
    Hero,
    TextImageSection
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/variables';

  .index{
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

</style>
