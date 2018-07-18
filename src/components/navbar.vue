<template>
  <div class="navbar">
    <div class="logo-div float-l m-l-40 m-r-25">
      <div class="logo"></div>
    </div>
    <a href="javascript:void(0);" id="hamburger"
       v-on:click="toggleNav()">
      <i class="fa fa-bars"></i>
    </a>
    <scrollactive id="nav-regular" class="unselectable"
                  :offset="0" :modifyUrl="false">
      <a v-for="page in navButtons" :href="page.id"
         class="scrollactive-item nav-btn">
        {{page.name}}
      </a>
    </scrollactive>
    <scrollactive id="nav-collapse" class="unselectable"
                  :class="{ visible: nav_show }"
                  :offset="0" :modifyUrl="false">
      <a v-for="page in navButtons" :href="page.id"
         class="scrollactive-item nav-btn">
        {{page.name}}
      </a>
    </scrollactive>
  </div>
</template>

<script>
import $ from 'jquery';
export default {
  name: 'navbar',
  components: {
  },
  data () {
    return {
      navButtons: [
        { name: 'home24',   route: '/',         id: '#home'    },
        { name: 'gallery',  route: '/gallery',  id: '#gallery' },
        { name: 'book',     route: '/book',     id: '#book'    },
        { name: 'rates',    route: '/rates',    id: '#rates'   },
        { name: 'contact',  route: '/contact',  id: '#contact' }
      ],
      nav_show: false,
      fullWidth: document.documentElement.clientWidth
    }
  },
  // bind event handlers to the `handleResize` method (defined below)
  mounted: function () {
    window.addEventListener('resize', this.handleResize)
  },
  beforeDestroy: function () {
    window.removeEventListener('resize', this.handleResize)
  },
  methods: {
    toggleNav() {
      this.nav_show = !this.nav_show;
    },
    // whenever the document is resized, re-set the 'fullHeight' variable
    handleResize (event) {
      this.fullWidth = document.documentElement.clientWidth
      //console.log(this.fullWidth)
      if (this.fullWidth >= 768) {
        this.nav_show = false;
      }
    }
  }
}

$(function() {
  var navbar = $(".navbar");
  var logo = $(".logo-div");
  var nav_regular = $("#nav-regular");
  var nav_collapse = $("#nav-collapse");
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
  $(window).resize( function() {
    this.nav_show = false;
    if ($(window).width() > 768) {
      //nav_regular.removeClass("collapse");
    } else {
      //nav_regular.addClass("collapse");
    }
  })
});
$(window).resize(function() {
  this.nav_show = false;
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
</style>
