<template>
  <b-row id="book">
    <b-col class="shade flex-y flex-align-start">
      <b-row class="text-center m-b-15">
        <b-col>
          <h2 class="color-bone">BOOK</h2>
        </b-col>
      </b-row>
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

      <b-row class="w-85percent m-t-10">
        <b-col sm="4" md="2">
          <b-form-group id="fieldset1"
                        label="Nights *">
            <v-select v-model="night_count" :options="guest_options"></v-select>
          </b-form-group>
        </b-col>
        <b-col sm="4" md="2">
          <b-form-group id="fieldset1"
                        label="Guests *">
            <v-select v-model="guest_count" :options="guest_options"></v-select>
          </b-form-group>
        </b-col>
        <b-col sm="4" md="2">
          <b-form-group label="Smoking">
            <b-form-checkbox id="checkbox-smoking"
                             v-model="smoking"
                             value="accepted"
                             unchecked-value="not_accepted">
              <i class="fas fa-smoking"></i>
            </b-form-checkbox>
          </b-form-group>
        </b-col>
        <b-col sm="12" md="6">
          <b-form-group id="fieldset1"
                        label="Room Type">
            <v-select class="" v-model="room_type" :options="room_types"></v-select>
          </b-form-group>
        </b-col>
      </b-row>

      <b-row class="m-y-10">
        <b-col>
          <button class="btn filled size-lg">check availability</button>
        </b-col>
      </b-row>

      <b-row class="w-85percent m-t-20">
        <b-col sm="12" md="8">
          <b-row>
            <b-col sm="12" md="6">
              <b-form-group id="fieldset1"
                            label="First Name">
                <b-form-input id="input1" v-model.trim="first_name"></b-form-input>
              </b-form-group>
            </b-col>
            <b-col sm="12" md="6">
              <b-form-group id="fieldset2"
                            label="Last Name">
                <b-form-input id="input2" v-model.trim="last_name"></b-form-input>
              </b-form-group>
            </b-col>
          </b-row>

          <b-row>
            <b-col sm="12" md="6">
              <b-form-group id="fieldset1"
                            label="E-mail">
                <b-form-input id="input1" v-model.trim="email"></b-form-input>
              </b-form-group>
            </b-col>
            <b-col sm="12" md="6">
              <b-form-group id="fieldset2"
                            label="Phone #">
                <b-form-input id="input2" v-model.trim="phone"></b-form-input>
              </b-form-group>
            </b-col>
          </b-row>
        </b-col>

        <b-col sm="12" md="4">
          <b-form-group id="notes"
                        label="Notes">
            <textarea name="notes" cols="4" class="h-95"></textarea>
          </b-form-group>
        </b-col>
      </b-row>

      <b-row class="w-85percent">
        <b-col sm="6" md="4">
          <b-form-group label="Airport Service">
            <b-form-checkbox id="checkbox-airport-car"
                             v-model="airport_service"
                             value="accepted"
                             unchecked-value="not_accepted">
              <i class="fas fa-car"></i>
            </b-form-checkbox>
          </b-form-group>
        </b-col>
        <b-col sm="6" md="4">
          <b-form-group id="fieldset2"
                        label="Pick-up Time">
            <b-form-input id="input2" v-model.trim="pickup_time"></b-form-input>
          </b-form-group>
        </b-col>
      </b-row>

      <b-row class="m-y-15">
        <b-col>
          <button class="btn filled size-lg">book</button>
        </b-col>
      </b-row>

    </b-col>
  </b-row>
</template>

<script>
export default {
  name: 'Book',
  components: {

  },
  data () {
    return {
      guest_options: [
        {id: 1, label: '1'},
        {id: 2, label: '2'},
        {id: 3, label: '3'},
        {id: 4, label: '4'},
        {id: 5, label: '5'},
        {id: 6, label: '6'},
        {id: 7, label: '7'},
        {id: 8, label: '8'},
        {id: 9, label: '9'},
        {id: 10, label: '10'},
        {id: 11, label: '11'},
        {id: 12, label: '12'}
      ],
      room_types: [
        { id: 0, label: 'Any' },
        { id: 1, label: 'Executive' },
        { id: 2, label: 'Deluxe' }
      ],
      checkin_date: '',
      checkout_date: '',
      night_count: undefined,
      guest_count: undefined,
      smoking: false,
      room_type: undefined,
      first_name: '',
      last_name: '',
      email: '',
      phone: '',
      airport_service: false,
      pickup_time: ''
    }
  }
}
</script>

<style scoped>
</style>
