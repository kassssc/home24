<template>
  <div id="app">
    <navbar></navbar>
    <!-- <router-view/> -->
    <home></home>
  </div>
</template>

<script>
import Navbar from './components/navbar'
import Home from './components/home'
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'
export default {
  name: 'App',
  components: {
    'navbar': Navbar,
    'home': Home
  },
  data () {
    return { title: 'Home24' }
  }
}
</script>

<style lang="scss">
//@import '../node_modules/bootstrap/scss/bootstrap.scss';
@import './styles/helpers.scss';
@import './styles/styles.scss';
@import './styles/images.scss';
@import './styles/navbar.scss';
@import './styles/calendar.scss';
</style>
