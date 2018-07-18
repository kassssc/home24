<template>
  <b-row id="rates">
    <b-col sm="12" md="8" class="flex-y p-50">
      <div class="carousel-container p-50">
        <b-carousel id="carousel1"
                    style="text-shadow: 1px 1px 2px #333;"
                    controls
                    indicators
                    background="#ababab"
                    :interval="4000"
                    v-model="slide"
                    @sliding-start="onSlideStart"
                    @sliding-end="onSlideEnd">

          <!-- Slides with img slot -->
          <!-- Note the classes .d-block and .img-fluid to prevent browser default image alignment -->
          <b-carousel-slide class="full-width full-height">
           <!--  <img slot="img" class="d-block img-fluid w-100" width="1024" height="480"
                src="https://picsum.photos/1024/480/?image=55" alt="image slot"> -->
            <img slot="img" class="d-block img-fluid w-100 full-width full-height"
                         src="https://picsum.photos/1024/480/?image=55" alt="image slot">
          </b-carousel-slide>
          <b-carousel-slide>
           <!--  <img slot="img" class="d-block img-fluid w-100" width="1024" height="480"
                src="https://picsum.photos/1024/480/?image=55" alt="image slot"> -->
            <img slot="img" class="d-block img-fluid w-100"
                         src="https://picsum.photos/1024/480/?image=55" alt="image slot">
          </b-carousel-slide>
        </b-carousel>
      </div>
    </b-col sm="12" md="4">
    <b-col class="p-x-20 flex-y">
      <div v-for="(style, index) in styles" class="style-card" v-on:click="select_type(index)" :class="{ active: selected_type == index}">
        <div class="type-title">{{style.name}}</div>
        <div class="types">
          <div v-for="type in style.types" class="type-container">
            <div>{{type.name}}</div>
            <div class="rate">฿{{type.rate[rate_index]}}</div>
          </div>
        </div>
      </div>
      <div class="rate-btn-container">
        <button v-for="(rate, index) in rates" class="rate-btn" v-on:click="select_rate(index)" :class="{active: index == rate_index}">
          {{rate}}
        </button>
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
