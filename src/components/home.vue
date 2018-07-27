<template>
  <b-container class="full-width full-height p-0" no-gutters="true">

    <b-row id="home">
      <b-col class="shade">
        <b-row>
          <b-col class="headline-container full-width unselectable">
            <div class="headline text-left">
              <h3 class="color-bone">Live <em>in</em></h3>
              <h1 class="color-bone">BANGKOK<br>CITY</h1>
              <h6 class="color-bone">Enjoy the City of Angels the right way</h6>
              <button v-scroll-to="'#gallery'" class="btn filled size-md m-y-10">
                gallery
              </button>
            </div>

          </b-col>
        </b-row>

        <b-row class="full-width m-0">
          <b-col sm="6" md="3">
            <b-form-group id="fieldset1"
                          label="Check-in *">
              <datepicker v-model="checkin_date" class="top"></datepicker>
              <i class="far fa-calendar-alt calendar-icon"></i>
            </b-form-group>
          </b-col>
          <b-col sm="6" md="3">
            <b-form-group id="fieldset1"
                          label="Check-out *">
              <datepicker v-model="checkout_date" class="top"></datepicker>
              <i class="far fa-calendar-alt calendar-icon"></i>
            </b-form-group>
          </b-col>
          <b-col sm="6" md="3">
            <b-form-group id="fieldset1"
                          label="Guests *">
              <v-select v-model="guest_count" :options="options" class="top"></v-select>
            </b-form-group>
          </b-col>
          <b-col sm="6" md="3">
            <button v-scroll-to="'#book'" class="btn filled full-width m-y-10">
              check availibility
            </button>
          </b-col>
        </b-row>

        <!-- <b-row class="h-50">
          <b-row class="w-85percent">
            <b-col sm="12" md="6">
              <b-form-group id="fieldset1"
                            label="Check-in *">
                <datepicker v-model="checkin_date"></datepicker>
                <i class="far fa-calendar-alt calendar-icon"></i>
              </b-form-group>
            </b-col>
            <b-col sm="12" md="6">
              <b-form-group id="fieldset1"
                            label="Check-out *">
                <datepicker v-model="checkout_date"></datepicker>
                <i class="far fa-calendar-alt calendar-icon"></i>
              </b-form-group>
            </b-col>
          </b-row>

          <b-col class="btn-container">
            <datepicker class="style-btn" placeholder="check-in date" v-model="checkin_date">
            </datepicker>
            <datepicker class="style-btn" placeholder="check-out date" v-model="checkout_date">

            </datepicker>
            <v-select class="" placeholder="guests" v-model="guests" :options="options"></v-select>
            <button class="btn outline size-lg" v-scroll-to="'#book'">book</button>
          </b-col>
        </b-row> -->

        <!-- Services -->
        <!-- <b-row class="h-50 m-t-50 p-x-30">
          <b-col class="services-container unselectable">
            <div class="service">
              <div class="icon-bts grow h-50 w-50 m-auto"></div>
              <div class="description float-b">
                <h6>Just steps away from<br>BTS Phrompong</h6>
              </div>
            </div>
            <div class="service">
              <div class="icon-em grow h-75 w-75 m-auto"></div>
              <div class="description float-b">
                <h6>Right beside The Emporium</h6>
                <h6>Across the street from Emquartier</h6>
              </div>
            </div>
            <div class="service">
              <div class="icon-breakfast grow h-45 w-45 m-auto"></div>
              <div class="description float-b">
                <h6>Complimentary<br>breakfast</h6>
              </div>
            </div>
            <div class="service">
              <div class="icon-wifi grow h-40 w-40 m-auto"></div>
              <div class="description float-b">
                <h6>Lightning fast WIFI</h6>
                <h6>thanks to Google Wifi routers</h6>
              </div>
            </div>
            <div class="service">
              <div class="icon-car grow h-45 w-45 m-auto"></div>
              <div class="description float-b">
                <h6>Airport car service available</h6>
              </div>
            </div>
            <div class="service">
              <div class="icon-parking grow h-35 w-35 m-auto"></div>
              <div class="description float-b">
                <h6>On-site parking available</h6>
                <h6>upon request prior to arrival</h6>
              </div>
            </div>
          </b-col>
        </b-row> -->

      </b-col>
    </b-row>

    <gallery></gallery>
    <book></book>
    <rates></rates>
    <contact></contact>
  </b-container>

<!--   <h1>h1 testing</h1><br>
<h2>h2 testing</h2><br>
<h3>h3 testing</h3><br>
<h4>h4 testing</h4><br>
<h5>h5 testing</h5><br>
<h6>h6 testing</h6><br> -->
</template>

<script>
import $ from 'jquery'
import Gallery from './gallery'
import Book from './book'
import Rates from './rates'
import Contact from './contact'

export default {
  name: 'Home',
  components: {
    'gallery': Gallery,
    'book': Book,
    'rates': Rates,
    'contact': Contact
  },
  data () {
    return {
      options: [
        {id: 1, label: '1'},
        {id: 2, label: '2'},
        {id: 3, label: '3'},
        {id: 4, label: '4'},
        {id: 5, label: '5'},
        {id: 6, label: '6'},
        {id: 7, label: '7'},
        {id: 8, label: '8'},
        {id: 9, label: '9'},
        {id: 10, label: '10'}
      ],
      guests: null,
      checkin_date: null,
      checkout_date: null
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
