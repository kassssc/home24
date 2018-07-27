<template>
  <b-row id="contact">
    <b-col class="shade p-x-0">
      <b-row class="full-width m-b-30">
        <b-col class="text-center">
          <h2 class="color-bone">CONTACT</h2>
        </b-col>
      </b-row>
      <b-row class="full-width">
        <b-col class="d-flex justify-content-end">
          <div class="google-maps w-450 h-350">
            <iframe
              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d968.9522160851049!2d100.56899652923198!3d13.730018899397603!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x30e29f01788d5a0f%3A0xe176b1e7bfcdcbc5!2sBKK+Home+24!5e0!3m2!1sen!2sth!4v1529246180925"
              width="450" height="350" frameborder="0" style="border:0">
            </iframe>
          </div>
        </b-col>
        <b-col class="justify-content-start">
          <div class="contact-container pointer">
            <div class="contact-field">
              <i class="fas fa-phone"></i>
              02-258-1818
            </div>
            <div class="copy-label">
              <i class="fas fa-copy"></i>COPY
            </div>
          </div>
          <div class="contact-container pointer">
            <div class="contact-field">
              <i class="fas fa-envelope"></i>
              reception@bkkhome24.com
            </div>
            <div class="copy-label">
              <i class="fas fa-copy"></i>COPY
            </div>
          </div>
          <div class="contact-container pointer">
            <div class="contact-field">
              <i class="fas fa-fax"></i>
              02-258-6488
            </div>
            <div class="copy-label">
              <i class="fas fa-copy"></i>COPY
            </div>
          </div>
          <div class="contact-container pointer">
            <div class="contact-field">
              <i class="fas fa-map-marked"></i>
              2/3-4 Sukhumvit 24<br>
              Khlong Tan, Khlong Toei<br>
              Bangkok 10110
            </div>
            <div class="copy-label">
              <i class="fas fa-copy"></i>COPY
            </div>
          </div>
          <div class="contact-container pointer">
            <div class="contact-field">
              <i class="fab fa-facebook-square"></i>
              @bkkhome24
            </div>
            <div class="copy-label">
              <i class="fas fa-link"></i>VISIT
            </div>
          </div>

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
