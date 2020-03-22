<template>
  <div>
    <Hero
      :heading="['Cooler', 'Text']"
    />
    <b-container
      class="my-5 py-5"
    >
      <b-row>
        <b-col>
          <h3 class="dashboard--second">
            Das sind unser Challenges
          </h3>
          <p class="dashboard--paragraph">
            Est veniam nostrud dolore officia. In tempor esse reprehenderit aliqua adipisicing aliqua aliquip adipisicing occaecat id enim. Exercitation nulla irure nulla aute proident duis exercitation aliquip ex do ullamco incididunt ut.
          </p>
        </b-col>
        <b-col class="text-center">
          <b-img src="/img/placeholder.jpg" fluid alt="Responsive image" width="300" />
        </b-col>
      </b-row>
    </b-container>
    <b-container class="my-5 py-5">
      <b-row>
        <b-col>
          <h3>
            Challenge erstellen
          </h3>
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
                />
              </b-form-group>

              <b-form-group id="input-group-2">
                <b-form-input
                  id="input-2"
                  v-model="form.text"
                  required
                  placeholder="Beschreibung der Challenge"
                />
              </b-form-group>
              <b-button>Upload Foto</b-button>
              <b-button>Upload Video</b-button>
              <br>
              <b-button type="submit" variant="primary" class="mt-4">
                Submit
              </b-button>
            </b-form>
          </div>
        </b-col>
      </b-row>
    </b-container>
    <b-container class="dashboard--challenges">
      <b-row>
        <b-col cols="9">
          <h3>Nimm jetzt an der Challenge teil</h3>
        </b-col>
        <b-col>
          <b-form>
            <b-form-group>
              <b-form-input
                id="input-1"
                required
                placeholder="Search"
              />
            </b-form-group>
          </b-form>
        </b-col>
      </b-row>
      <div v-for="challenge in challenges" :key="challenge.id">
        <ChallengeCard
          :id="challenge.id"
          :title="challenge.title"
          :text="challenge.text"
        />
      </div>
    </b-container>
    </hero>
  </div>
</template>

<script>
import ChallengeCard from '../../components/ChallengeCard'
import Hero from '../../components/dashboard/Hero'
export default {
  components: {
    ChallengeCard,
    Hero
  },
  data () {
    return {
      challenges: [],
      form: {
        title: '',
        text: ''
      }
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
}
</style>
