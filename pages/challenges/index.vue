<template>
  <div>
    <Hero
      :heading="['Nie mehr Langeweile', 'allein zu Haus!']"
    />
    <TextImageSection
      :heading="['Verwende deine Zeit', 'sinnvoll']"
      text="  Ipsum elit magna est sunt amet. Qui aute culpa irure cillum adipisicing minim ad dolore cillum id commodo occaecat adipisicing. Sit tempor ad nostrud est fugiat aliquip do enim sit culpa voluptate officia. Pariatur ullamco cillum laborum adipisicing nulla laboris amet do. Aliqua quis sunt duis ut eu magna ex aliqua nostrud aliquip sint duis elit. Sunt anim culpa ad irure minim non fugiat cillum mollit pariatur ipsum irure."
      img-link="/img/blob1.png"
      img-pos="right"
    />
    <b-container class="my-5 py-5">
      <b-row>
        <b-col>
          <div class="dashboard--card">
            <b-form @submit="onSubmit" @reset="onReset">
              <b-form-group
                id="input-group-1"
              >
                <b-form-input
                  id="input-1"
                  v-model="form.title"
                  required
                  placeholder="Name der Challenge"
                  class="dashboard--input"
                />
              </b-form-group>

              <b-form-group id="input-group-2">
                <b-form-input
                  id="input-2"
                  v-model="form.text"
                  required
                  placeholder="Beschreibung der Challenge"
                  class="dashboard--input mt-4"
                />
              </b-form-group>
              <b-row class=" my-4">
                <div v-for="categorie in categories" :key="categorie.title" class="dashbord--categories">
                  <b-col>
                    <div :class="form.categorie === categorie.title ? 'dashboard--categorie-active' : 'dashboard--categorie'" @click="handleCategorie(categorie.title)">
                      <b-img
                        :src="form.categorie === categorie.title ? `/icon/${categorie.icon}-white.png` : `/icon/${categorie.icon}.png`"
                        class="dashboard--icon"
                      />
                      <h6>
                        {{ categorie.title }}
                      </h6>
                    </div>
                  </b-col>
                </div>
              </b-row>
              <b-button class="btn--secondary mr-3" @click="foto = !foto">
                {{ foto ? "Remove Foto" : "Upload Foto" }}
              </b-button>
              <b-button class="btn--secondary" @click="video = !video">
                {{ video ? "Remove video" : "Upload video" }}
              </b-button>
              <b-form-input
                v-if="foto"
                id="input-2"
                v-model="form.fotoLink"
                required
                placeholder="Foto Link"
                class="dashboard--input mt-4"
              />
              <b-form-input
                v-if="video"
                id="input-2"
                v-model="form.videoLink"
                required
                placeholder="Video Link"
                class="dashboard--input mt-4"
              />
              <br>
              <b-button type="submit" variant="primary" class="mt-4">
                Fertigstellen
              </b-button>
            </b-form>
          </div>
        </b-col>
      </b-row>
    </b-container>
    <b-container class="dashboard--challenges my-5 py-5">
      <b-row>
        <b-col cols="9">
          <h3>Nimm jetzt an der Challenge <span class="highlighted">teil</span></h3>
        </b-col>
        <b-col>
          <b-form>
            <b-form-group>
              <b-form-input
                id="input-1"
                v-model="search"
                required
                placeholder="Search"
                class="dashboard--input"
              />
            </b-form-group>
          </b-form>
        </b-col>
      </b-row>
      <div v-for="challenge in challenges" :key="challenge.id">
        <div v-for="categorie in categories" :key="categorie.title">
          <ChallengeCard
            v-if="challenge.categorie === categorie.title"
            :id="challenge.id"
            :title="challenge.title"
            :text="challenge.text"
            :categorie="challenge.categorie"
            :foto-link="challenge.fotoLink"
          />
        </div>
      </div>
    </b-container>
  </div>
</template>

<script>
import ChallengeCard from '../../components/ChallengeCard'
import Hero from '../../components/dashboard/Hero'
import TextImageSection from '../../components/dashboard/TextImageSection'

export default {
  components: {
    ChallengeCard,
    Hero,
    TextImageSection
  },
  data () {
    return {
      challenges: [{
        title: '1 Stunde Yoga',
        text: 'Sit dolor laborum ut tempor voluptate in labore elit anim voluptate et excepteur. Laborum duis exercitation enim nulla occaecat commodo sit et dolor officia tempor. Adipisicing cupidatat nulla Lorem exercitation velit pariatur quis proident officia aute proident tempor irure eiusmod. Nisi excepteur labore excepteur exercitation esse adipisicing aliquip amet nisi nisi. Esse esse adipisicing sit aliquip consectetur velit dolore. Sint eiusmod ea id labore elit sit ipsum sit ipsum officia.',
        categorie: 'Sport'
      }],
      categories: [{
        title: 'Sport',
        icon: 'sport'
      },
      {
        title: 'Charity',
        icon: 'heart'
      },
      {
        title: 'Kreativität',
        icon: 'light'
      },
      {
        title: 'Haushalt',
        icon: 'house'
      },
      {
        title: 'Spaß',
        icon: 'fun'
      }
      ],
      form: {
        title: '',
        text: '',
        categorie: '',
        fotoLink: ''
      },
      foto: false,
      video: false,
      search: ''
    }
  },
  methods: {
    onSubmit (evt) {
      evt.preventDefault()
      this.challenges.push(this.form)
    },
    onReset (evt) {
      evt.preventDefault()
      // Reset our form values
      this.form.title = ''
      this.form.text = ''
      this.form.categorie = ''
      this.form.fotoLink = ''
    },
    handleCategorie (categorie) {
      this.form.categorie = categorie
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/variables';

.dashboard{
  &--hero{
    background-image: url('/img/placeholder.jpg');
    background-position:  bottom;
    background-size: cover;
    height: 50vh;
    background-attachment: fixed;
  }
  &--heading{
    background: $linear-gradient;
    border-radius: 7px;
    color: white;
    padding: 1.2rem;
  }
  &--second{
    color: $primary;
    background-color: $background;
    padding: .5rem;
    border-radius: 7px;
  }
  &--paragraph{
    color: $text-color;
    font-weight: 500;
    padding: 1rem .5rem;
  }
  &--card{
    box-shadow: 4px 4px 10px rgba(0, 0, 0, 0.25);
    padding: 3rem 6rem;
    margin-top: 2rem;
  }
  &--challenges{
    min-height: 20vh;
  }
  &--input{
    border-top: none;
    border-left: none;
    border-right: none;
    border-radius: 0px;
    border-color: $primary;
  }
  &--categorie{
    border: 1px solid $primary;
    width: 120px;
    height: 70px;
    color: $primary;
    border-radius: 3px;
    text-align: center;
    padding: .5rem;
    margin: 1.5rem 0rem;
    cursor: pointer;
    > h6{
      font-weight: lighter;
      font-size: 15px;
    }
  }

  &--categorie-active{
    border: 1px solid $primary;
    cursor: pointer;
    width: 120px;
    height: 70px;
    color: white;
    border-radius: 3px;
    text-align: center;
    background-color: $primary;
    padding: .5rem;
    margin: 1.5rem 0rem;
  }
  @media only screen and (max-width: 420px){
    &--categorie, &--categorie-active{
      width: 65px;
      height: 60px;
      margin: .5rem 0rem;
      padding: .1rem;
      > h6{
        font-size: 12px;
        text-align: center;
      }
    }
    &--card {
    padding: 2rem 1rem;
    margin-top: 2rem;
  }
  }

}
</style>
