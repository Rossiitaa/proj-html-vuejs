<template>
  <div id="app">
    <Header />
    <Jumbotron />
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'
import Jumbotron from './components/Jumbotron.vue'

export default {
  name: 'App',
  components: {
    Header,
    Jumbotron,
    Main,
    Footer
    
  }
}
</script>

<style lang="scss" >
@import url('https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@200&display=swap');
@import '~bootstrap/scss/bootstrap.scss';
@import './styles/general.scss';

</style>
