<template lang="pug">
  .stars-wrapper#scene
    .layer(data-depth="0.00")
    .stars-cluster.stars-cluster-1.layer(data-depth="0.30")
      - for (var x = 1; x <=40; x++)
        .star(class="star-"+x)
    .stars-cluster.stars-cluster-2.layer(data-depth="0.50")
      - for (var x = 1; x <=40; x++)
        .star(class="star-"+x)
    .stars-cluster.stars-cluster-3.layer(data-depth="0.90")
      - for (var x = 1; x <=15; x++)
        .star(class="star-"+x)
    .moon-wrapper.layer(data-depth="0.30")
      .moon
    .title-wrapper.layer(data-depth="0.40")
      h1.title(data-title="Fly me to the moon") Fly me to the moon
</template>
<style lang="less">
  @import "../assets/less/winter.less";
  @import "https://cdnjs.cloudflare.com/ajax/libs/normalize/5.0.0/normalize.min.css";
</style>
<script>
  import $ from 'jquery'
  require("imports?$=jquery!../assets/js/jquery.parallax.js")
  $(function() {
    $('#scene').parallax({
      calibrateX: true,
      calibrateY: true,
      scalarX: 12,
      scalarY: 12,
      frictionX: 0.1,
      frictionY: 0.1,
      originX: 0.5,
      originY: 0.5
    });
  });

    export default{
        name:'Winter',
        data(){
            return{
                msg:'hello vue'
            }
        }
    }
</script>
