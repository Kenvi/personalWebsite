<template>
  <div id="app">
    <div class="fakeloader"></div>
    <winter></winter>
  </div>
</template>
<style>
  @import "assets/css/fakeLoader.css";
</style>
<script>
import Winter from './components/Winter'
import $ from 'jquery'
require("imports?jQuery=jquery!./assets/js/fakeLoader.js")

export default {
  name: 'app',
  components: {
    Winter
  },
  mounted:function () {
    $(document).ready(function(){
      $(".fakeloader").fakeLoader({
        timeToHide:2000,
        bgColor:"#02080f",
        spinner:"spinner7"
      });
    });

  }
}
</script>

