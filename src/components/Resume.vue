<template lang="pug">
  #resume-main
    .resume-tab-wrap
      ul.resume-tab-menu
        li.active
          a(href='##',data-tab='1')
            span.icon.icon-glass
            span.menu-text Profile
        li
          a(href='##',data-tab='2')
            span.icon.icon-glass
            span.menu-text Education
        li
          a(href='##',data-tab='3')
            span.icon.icon-glass
            span.menu-text Experience
        li
          a(href='##',data-tab='4')
            span.icon.icon-glass
            span.menu-text Skills
  //  .resume-tab-content.active(data-content='1')
        .resume-tab-inner.text-center
          .row.row-bottom-padded-sm
            .col-md-12
              figure
                h1 Chen Xiaobin
                p 121212

</template>
<style lang="less">
  body{
    background: #fff;
  }
  @import "../assets/less/resume.less";
</style>
<script>
  export default{
    name:'Resume',
    data(){
      return{
        msg:'hello vue'
      }
    },
    components:{

    }
  }
</script>
