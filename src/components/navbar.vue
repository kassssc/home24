<template>
  <!-- <div class="navbar">
    <div class="logo-div float-l h-75 w-300 m-l-50 m-r-50">
      <div class="logo"></div>
    </div>
    <div class="float-r m-r-50 min-w-400">
      <div v-for="page in navButtons" class="float-l">
        <router-link :to="{path:page.route}">
        <button v-scroll-to="page.id" class="btn nav-btn">
          {{page.name}}
        </button>
        </router-link>
      </div>
    </div>
  </div> -->

</template>

<script>
import TitleLogo from './title-logo';
import $ from 'jquery';
export default {
  name: 'nav',
  components: {
    'title-logo': TitleLogo
  },
  data () {
    return {
      navButtons:
        [
          { name: 'home24',   route: '/' , id: '#home' },
          { name: 'gallery',  route: '/gallery' , id: '#gallery'},
          { name: 'rates',    route: '/rates' , id: '#rates' },
          { name: 'book',     route: '/book' , id: '#home' },
          { name: 'contact',  route: '/contact' , id: '#contact' }
        ]
    }
  }
}

$(function() {
  var navbar = $(".navbar");
  var logo = $(".logo-div");
  $(window).scroll(function() {
    var scroll = $(window).scrollTop();

    if (scroll >= 25) {
      navbar.addClass("darken");
      logo.addClass("shrink");
    } else {
      navbar.removeClass("darken");
      logo.removeClass("shrink");
    }
  });
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
</style>
