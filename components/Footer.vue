<template>
  <footer class="d-flex">
    <b-container fluid class="elements text-center">
      <b-row>
        <b-col offset="3">
          Challenge erstellen
        </b-col>
        <b-col>
          Challenge erstellen
        </b-col>
        <b-col>
          Impressum
        </b-col>
        <b-col>
          Datenschutz
        </b-col>
      </b-row>
    </b-container>
  </footer>
</template>

<script>

</script>

<style lang="scss" scoped>
@import '../assets/style/variables';

    footer{
        height: 5vh;
        background-color: $secondary;
        color: white;
        > .elements{
          margin-top: auto;
          margin-bottom: auto;
        }
    }
</style>
