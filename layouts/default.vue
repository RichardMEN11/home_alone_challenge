<template>
  <div>
    <Nav />
    <nuxt />
    <Footer />
  </div>
</template>
<script>
import Nav from '../components/Nav'
import Footer from '../components/Footer'

export default {
  components: {
    Nav,
    Footer
  }
}
</script>
<style lang="scss">
@import '../assets/style/variables';

html {
  font-family: 'Helvetica', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

a {
  text-decoration: none;
  color: #37384F;
}

a:hover{
  text-decoration: none;
  color: #37384F;
}

.nuxt-link-exact-active{
  text-decoration: none;
  color: $primary;
}

.btn-primary {
  color: white;
  background-color: $primary;
  border: none;
  padding: 1rem 2.5rem;
  border-radius: 7px;
}
.btn-primary--outline {
  color: $primary;
  border: 1px solid $primary;
  padding: .5rem 2.5rem;
  border-radius: 7px;
}
.btn-primary--outline:hover {
  color: $secondary;
  text-decoration: none;
  border: 1px solid $secondary;
  padding: .5rem 2.5rem;
  border-radius: 7px;
}
.btn-secondary--outline {
  color: $secondary;
  border: 1px solid $secondary;
  padding: .5rem 2.5rem;
  border-radius: 7px;
}
.btn-secondary--outline:hover {
  color: $primary;
  text-decoration: none;
  border: 1px solid $primary;
  padding: .5rem 2.5rem;
  border-radius: 7px;
}

.btn-primary:hover {
  text-decoration: none;
  background-color: $secondary;
  color: white;
}

.btn-secondary{
  background-color: $lg-background;
  border: none;
  border-radius: 18px;
  color: #000;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}

.highlighted{
    color: $primary;
  }

.input[type="text"]:focus{
  outline: none !important;
}
</style>
