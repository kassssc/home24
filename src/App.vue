<template>
  <div id="app">
    <navbar></navbar>
    <router-view/>
  </div>
</template>

<script>
import Navbar from './components/navbar'
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'
export default {
  name: 'App',
  components: {
    'navbar': Navbar
  },
  data () {
    return { }
  }
}
</script>

<style lang="scss">
@import './styles/helpers.scss';
@import './styles/styles.scss';
@import './styles/images.scss';
@import './styles/navbar.scss';
@import './styles/inputs.scss';
</style>
