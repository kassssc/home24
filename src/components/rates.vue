<template>
  <b-row id="rates" class="no-gutter">
    <b-col sm="12" md="8" class="flex-y p-50">
      <b-carousel id="carousel1"
                  style="text-shadow: 1px 1px 2px #333;"
                  controls
                  indicators
                  background="#ababab"
                  :interval="4000"
                  v-model="slide"
                  img-width="1024"
                  img-height="550"
                  @sliding-start="onSlideStart"
                  @sliding-end="onSlideEnd">

        <b-carousel-slide caption="Blank Image" img-blank img-alt="Blank image"></b-carousel-slide>
        <b-carousel-slide caption="Blank Image" img-blank img-alt="Blank image"></b-carousel-slide>
        <b-carousel-slide caption="Blank Image" img-blank img-alt="Blank image"></b-carousel-slide>
      </b-carousel>
    </b-col sm="12" md="4">

    <b-col class="p-x-20 d-flex flex-column justify-content-center">
      <div class="d-flex flex-column justify-content-between h-450">
        <div class="style-div">
          <div v-for="(style, index) in styles" class="style-card" v-on:click="select_type(index)" :class="{ active: selected_type == index}">
            <div class="type-title">{{style.name}}</div>
            <div class="types">
              <div v-for="type in style.types" class="type-container">
                <div>{{type.name}}</div>
                <div class="rate">฿{{type.rate[rate_index]}}</div>
              </div>
            </div>
          </div>
        </div>
        <div class="rate-btn-container">
          <button v-for="(rate, index) in rates" class="rate-btn" v-on:click="select_rate(index)" :class="{active: index == rate_index}">
            {{rate}}
          </button>
        </div>
      </div>
    </b-col>
  </b-row>
</template>

<script>
export default {
  name: 'Rates',
  components: {

  },
  data () {
    return {
      slide: 0,
      sliding: null,
      selected_type: 0,
      rate_index: 0,
      styles: [
        {
          name: 'sukhothai',
          types: [
            {
              name: 'executive',
              rate: [
                2800,
                2600,
                2200
              ]
            }
          ]
        },
        {
          name: 'ayutthaya',
          types: [
            {
              name: 'executive',
              rate: [
                2800,
                2600,
                2200
              ]
            },
            {
              name: 'deluxe',
              rate: [
                2300,
                2200,
                1900
              ]
            }
          ]
        },
        {
          name: 'lanna',
          types: [
            {
              name: 'executive',
              rate: [
                2800,
                2600,
                2200
              ]
            },
            {
              name: 'deluxe',
              rate: [
                2300,
                2200,
                1900
              ]
            }
          ]
        },
        {
          name: 'bangkok',
          types: [
            {
              name: 'deluxe',
              rate: [
                2300,
                2200,
                1900
              ]
            }
          ]
        },
      ],
      rates: [
        'nightly',
        'weekly',
        'monthly'
      ]
    }
  },
  methods: {
    onSlideStart (slide) {
      this.sliding = true
    },
    onSlideEnd (slide) {
      this.sliding = false
    },
    select_type (type) {
      this.selected_type = type
    },
    select_rate (rate) {
      this.rate_index = rate
    }
  }
}
</script>

<style lang="scss" scoped>
</style>
