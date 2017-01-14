<template lang="pug">
  #resume-main
    .resume-tab-wrap
      ul.resume-tab-menu
        li
          a(href='##',data-tab='1')
            span.iconfont.icon-bussinessman
            span.menu-text 个人简介
        li.active
          a(href='##',data-tab='2')
            span.iconfont.icon-office
            span.menu-text 校内经历
        li
          a(href='##',data-tab='3')
            span.iconfont.icon-form
            span.menu-text 工作经历
        li
          a(href='##',data-tab='4')
            span.iconfont.icon-lights
            span.menu-text 掌握技能
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
              td.pr-size 职业：前端工程师
          p {{intro}}
          p {{hobby}}
      .resume-tab-content(data-content='2')
        .resume-content-inner
          p.ta-c 本科专业课程（数字媒体技术）及社团实践中掌握了的知识
          .resume-feature
            .resume-icon
              i.iconfont.icon-training
            .resume-text
              h2 2012-2013
              p 熟悉素描，色彩原理，了解物体透视原理，色彩构成原理。掌握软件Ps的基本工具操作。
          .resume-feature
            .resume-icon
              i.iconfont.icon-imagetext
            .resume-text
              h2 2013-2014
              p 担任校学生新闻中心数媒部部长，掌握包括Ps，Ae，Pr等相关设计及视频制作软件。参与校刊《广东工业大学报》、《工大学子》的排版设计。
          .resume-feature
            .resume-icon
              i.icon-graduation-cap
            .resume-text
              h2 2014-2015
              p
</template>
<style lang="less">
  body{
    background: #fff;
  }

  @import "//at.alicdn.com/t/font_4w5wlo8gsibmlsor.css";
  @import "../assets/less/resume.less";
  /*#resume-main{height:1000px}*/
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
    }
  }
</script>
