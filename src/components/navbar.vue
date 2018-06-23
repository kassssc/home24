<template>
  <div class="navbar">
    <div class="logo-div float-l h-75 w-300 m-l-50 m-r-50">
      <div class="logo"></div>
    </div>
    <scrollactive class="nav-buttons" :offset="0">
      <a v-for="page in navButtons"
         :href="page.id"
         class="scrollactive-item nav-btn">
        {{page.name}}
      </a>
    </scrollactive>
  </div>
</template>

<script>
import $ from 'jquery';
export default {
  name: 'nav',
  components: {
  },
  data () {
    return {
      navButtons:
        [
          { name: 'home24',   route: '/' , id: '#home' },
          { name: 'gallery',  route: '/gallery' , id: '#gallery'},
          { name: 'book',     route: '/book' , id: '#book' },
          { name: 'rates',    route: '/rates' , id: '#rates' },
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
