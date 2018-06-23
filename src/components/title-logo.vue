<template>
  <div class="container">
    <h1>{{title}}</h1>
  </div>
</template>

<script>
export default {
  name: 'title-logo',
  data () {
    return {
      title: 'Home 24'
    }
  }
}
</script>

<style lang="scss" scoped>
.container {
  float: left;
  background: transparent;
  padding-left: 0px;
  margin-bottom: 20px;
  h1 {
    font-weight: 900;
    font-size: 50px;
    color: #444444;
  }
}
</style>
