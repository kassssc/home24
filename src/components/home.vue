<template>

  <b-container class="content p-0">


 <!-- HOME -->
    <b-row id="home">
      <b-col class="shade">
        <b-row>
          <b-col class="headline full-width min-w-600 text-center unselectable">
            <h4 class="color-bone">Home24 Boutique Hotel</h4>
            <h1 class="color-bone">Live <em>in</em> Bangkok City</h1>
          </b-col>
        </b-row>

        <b-row class="h-50 m-b-30">
          <b-col class="btn-container">
            <button v-scroll-to="'#gallery'" class="btn outline size-lg m-x-15">
              gallery
            </button>
            <button v-scroll-to="'#rates'" class="btn outline size-lg m-x-15">
              rates
            </button>
          </b-col>
        </b-row>

        <b-row class="h-50 m-t-50">
          <b-col class="btn-container">
            <button class="btn outline size-lg m-x-15">check-in</button>
            <button class="btn outline size-lg m-x-15">check-out</button>
            <!-- <button class="btn outline size-lg m-x-15">guests</button> -->
            <v-select class="m-x-15" v-model="selected" :options="options"></v-select>
            <button class="btn outline size-lg m-x-15">book</button>
          </b-col>
        </b-row>
        <!-- Services -->
        <b-row class="h-50 m-t-50 p-x-30">
          <b-col class="services-container unselectable">
            <div class="service">
              <div class="icon-bts grow h-70 w-70 m-auto"></div>
              <div class="description float-b">
                <h6>Just steps away from<br>BTS Phrompong</h6>
              </div>
            </div>
            <div class="service">
              <div class="icon-em grow h-100 w-100 m-auto"></div>
              <div class="description float-b">
                <h6>Right beside The Emporium</h6>
                <h6>Across the street from Emquartier</h6>
              </div>
            </div>
            <div class="service">
              <div class="icon-breakfast grow h-85 w-85 m-auto"></div>
              <div class="description float-b">
                <h6>Complimentary<br>breakfast</h6>
              </div>
            </div>
            <div class="service">
              <div class="icon-wifi grow h-60 w-60 m-auto"></div>
              <div class="description float-b">
                <h6>Lightning fast WIFI</h6>
                <h6>thanks to Google Wifi routers</h6>
              </div>
            </div>
            <div class="service">
              <div class="icon-car grow h-65 w-65 m-auto"></div>
              <div class="description float-b">
                <h6>Airport car service available</h6>
              </div>
            </div>
            <div class="service">
              <div class="icon-parking grow h-45 w-45 m-auto"></div>
              <div class="description float-b">
                <h6>On-site parking available</h6>
                <h6>upon request prior to arrival</h6>
              </div>
            </div>
          </b-col>
        </b-row>

      </b-col> <!-- END home-col -->
    </b-row> <!-- END HOME -->

    <gallery></gallery>
    <book></book>
    <rates></rates>
    <contact></contact>
  </b-container>

</template>

 <!-- <div class="b-row m-t-100">
   <datepicker :inline="true"></datepicker>
   <div class="h-500 w-500">
     <h1>h1 testing</h1><br>
     <h2>h2 testing</h2><br>
     <h3>h3 testing</h3><br>
     <h4>h4 testing</h4><br>
     <h5>h5 testing</h5><br>
     <h6>h6 testing</h6><br>
   </div>
 </div> -->

<script>
import Gallery from './gallery'
import Book from './book'
import Rates from './rates'
import Contact from './contact'
import Datepicker from 'vuejs-datepicker'
import $ from 'jquery'

export default {
  name: 'Home',
  components: {
    'gallery': Gallery,
    'book': Book,
    'rates': Rates,
    'contact': Contact,
    'date-picker': Datepicker,
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      options: [
        {id: 1, label: '1'},
        {id: 2, label: '2'},
        {id: 3, label: '3'},
        {id: 4, label: '4'},
        {id: 5, label: '5'}
      ],
      selected: null,
    }
  }
}
</script>
import $ from 'jquery';
$('.datepicker').datepicker();
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
