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
      .resume-tab-content.active(data-content='1')
        .resume-content-inner
          figure
            img(src='../assets/images/portrait.png',width='140px',alt='portrait')
          h1 陈晓斌
          table
            tr
              td 年龄：23
              td 学校：广东工业大学
            tr
              td 电话：136 1146 9741
              td 专业：数字媒体技术
            tr
              td 邮箱：604113530@qq.com
              td(style='padding-right:20px') 职业：前端工程师
          p {{intro}}
          p {{hobby}}
</template>
<style lang="less">
  body{
    background: #fff;
  }
  @import "../assets/less/resume.less";
  #resume-main{height:1000px}
</style>
<script>
  export default{
    name:'Resume',
    data(){
      return{
        intro:'广东云浮罗定人，2016年毕业于广东工业大学数字媒体技术专业，2015年5月开始实习，一直从事前端开发相关工作。' +
              '曾参与某国有银行网银系统内部开发，有p2p金融平台前端开发经验；' +
              '曾使用node.js+express+mongoDB独立开发某绿化公司宣传网站；' +
              '有微信公众号开发经验（对微信公众平台接口调用亦有所了解）。' +
              '熟练mv*开发模式（有vue.js开发经验），熟悉前端管理方案（了解gulp及webpack），熟悉node.js。' +
              '熟练Ps，Ai等设计软件的使用。',
        hobby:'喜欢各类体育运动，喜欢旅游，喜欢摄影，喜欢电影，喜欢音乐，喜欢K歌，吃货。'
      }
    },
    components:{

    }
  }
</script>
