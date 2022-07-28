<template>
  <div id="app">
    <Header />
    <Jumbotron1 />
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'
import Jumbotron1 from './components/Jumbotron1.vue'

export default {
  name: 'App',
  components: {
    Header,
    Jumbotron1,
    Main,
    Footer
    
  }
}
</script>

<style lang="scss" >
@import url('https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@200&display=swap');
@import '~bootstrap/scss/bootstrap.scss';
@import './styles/general.scss';

* {
  font-family: 'Nunito', sans-serif;
  font-weight: 400;
}

</style>
