<template>
  <b-row id="contact">
    <b-col class="shade">
      <b-row class="full-width min-w-600 m-b-30">
        <b-col class="text-center">
          <h2 class="color-bone">CONTACT</h2>
        </b-col>
      </b-row>
      <b-row>
        <b-col>
          <div class="google-maps m-auto w-455 h-355">
            <iframe
              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d968.9522160851049!2d100.56899652923198!3d13.730018899397603!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x30e29f01788d5a0f%3A0xe176b1e7bfcdcbc5!2sBKK+Home+24!5e0!3m2!1sen!2sth!4v1529246180925"
              width="450" height="350" frameborder="0" style="border:0">
            </iframe>
          </div>
        </b-col>
        <b-col>
          <h5 class="color-bone">02-258-1818</h5>
          <h5 class="color-bone">reservation@bkkhome24.com</h5>
        </b-col>
      </b-row>
    </b-col>
  </b-row> <!-- END CONTACT -->
</template>

<script>
export default {
  name: 'Contact',
  components: {

  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<style scoped>
</style>
