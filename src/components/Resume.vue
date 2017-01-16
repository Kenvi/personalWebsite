<template lang="pug">
  #resume-main
    .resume-tab-wrap
      ul.resume-tab-menu
        li
          a(href='##',data-tab='1')
            span.iconfont.icon-bussinessman
            span.menu-text 个人简介
        li
          a(href='##',data-tab='2')
            span.iconfont.icon-office
            span.menu-text 校内经历
        li.active
          a(href='##',data-tab='3')
            span.iconfont.icon-history
            span.menu-text 工作经历
        li
          a(href='##',data-tab='4',data-pie="yes")
            span.iconfont.icon-lights
            span.menu-text 掌握技能
      .resume-tab-content(data-content='1')
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
          p 喜欢各类体育运动，喜欢旅游，喜欢摄影，喜欢电影，喜欢音乐，喜欢K歌，吃货。
      .resume-tab-content(data-content='2')
        .resume-content-inner
          p.ta-c 本科专业课程（数字媒体技术）及社团实践中掌握了的知识
          .resume-feature
            .resume-icon
              i.iconfont.icon-Ps
            .resume-text
              h2 2012-2013
              p 熟悉素描，色彩原理，了解物体透视原理，色彩构成原理。掌握软件Ps的基本工具操作。
          .resume-feature
            .resume-icon
              i.iconfont.icon-news
            .resume-text
              h2 2013-2014
              p 担任校学生新闻中心数媒部部长，掌握包括Ps，Ae，Pr等相关设计及视频制作软件。参与校刊《广东工业大学报》、《工大学子》的排版设计。
          .resume-feature
            .resume-icon
              i.iconfont.icon-js
            .resume-text
              h2 2014-2015
              p 正式开始前端之路，熟练掌握html+css静态页面构建，了解html5及css3新特性，掌握各浏览器兼容问题，熟练使用jQuery对页面进行dom操作。
          .resume-feature
            .resume-icon
              i.iconfont.icon-weixin
            .resume-text
              h2 2015-2016
              p 熟悉微信公众号开发，熟练掌握微信js-sdk的使用。熟练掌握bootstrap，熟练掌握less等css预处理技术。熟悉mvc开发模式，了解网站后台及数据库工作原理。熟练svn，git等代码管理工具。
          .resume-feature
            .resume-icon
              i.iconfont.icon-node
            .resume-text
              h2 2016-2016.9
              p 熟悉node.js，熟悉微信公众平台接口调用，熟悉mongoDB。了解ES6，前端自动化构建，前端模块化思想。了解前端mvvm开发模式，掌握vue.js+webpack+vue-router开发SPA。
      .resume-tab-content(data-content='3')
        .resume-content-inner
          p.ta-c 项目及工作经历
          .resume-feature
            .resume-icon
              i.iconfont.icon-form
            .resume-text
              h2 2015.05-2015.06
              p 加入广州睿程科技有限公司并担任前端开发工程师，参与某国有银行网上银行网站系统内部开发。
          .resume-feature
            .resume-icon
              i.iconfont.icon-form
            .resume-text
              h2 2015.09-2016.03
              p 加入广州快悦信息科技公司，负责旗下小金瓜投资理财网的pc及微信的开发及维护工作。
                a(href='https://www.xiaojingua.com/',target='_blank') (https://www.xiaojingua.com/)
          .resume-feature
            .resume-icon
              i.iconfont.icon-training
            .resume-text
              h2 2016.03-2016.06
              p 使用node.js+express+mongoDB独立开发某绿化公司的企业宣传网站，实现包括新建产品，产品分类，产品推荐，产品搜索，banner上传，发布消息等功能。
          .resume-feature
            .resume-icon
              i.iconfont.icon-form
            .resume-text
              h2 2016.06-2016.10
              p 加入广州铭信网标网络科技有限公司，负责旗下社交分享产品“玩啥”的公众号开发及维护工作。
          .resume-feature
            .resume-icon
              i.iconfont.icon-training
            .resume-text
              h2 2016.10-2016.12
              p 负责公司新项目“聚焦分享”的pc端页面(包括内容编辑，数据处理)开发及维护工作。
                a(href='http://share.mofor.cn/',target='_blank') (http://share.mofor.cn/)
      .resume-tab-content.active(data-content='4')
        .resume-content-inner
          p.ta-c 掌握技能
          .row
            .item(v-for='n in 16')
              .chart(data-percent="95")
                span
                  strong HTML5
                  i 95%
                canvas(height='150',width='150',style='width:130px;height:130px;')
</template>
<style lang="less">
  @import "//at.alicdn.com/t/font_13h4f0kd25xnipb9.css";
  @import "../assets/less/resume.less";
</style>
<script>
  import $ from 'jquery'
  require("imports?$=jquery!../assets/js/jquery.easypiechart.min.js")

  var getHeight = function() {
    var extraHeight = 0;


    setTimeout(function(){
      $('#resume-main').stop().animate({
        'height': $('.resume-tab-content.active').height() + extraHeight
      });
    }, 200);
  };

  var pieChart = function() {
    $('.chart').easyPieChart({
      scaleColor: false,
      lineWidth: 5,
      lineCap: 'butt',
      barColor: '#bcd1ff',
      trackColor:	"#000000",
      size: 100,
      animate: 1000
    });
  };

  var tabContainer = function() {
    getHeight();
    $(window).resize(function(){
      getHeight();
    })
  };

  var tabClickTrigger = function() {
    $('.resume-tab-menu a').on('click', function(event) {
      event.preventDefault();
      var $this = $(this),
        data = $this.data('tab'),
        pie = $this.data('pie');

      // add/remove active class
      $('.resume-tab-menu li').removeClass('active');
      $this.closest('li').addClass('active');

      $('.resume-tab-content.active').addClass('animated fadeOutDown');

      setTimeout(function(){
        $('.resume-tab-content.active').removeClass('active animated fadeOutDown fadeInUp');
        $('.resume-tab-content[data-content="'+data+'"]').addClass('animated fadeInUp active');
        getHeight();
      }, 500);

      if ( pie === 'yes' ) {
        setTimeout(function(){
          pieChart();
        }, 800);
      }

    })
  };

  // Document on load.
  $(function(){
    tabContainer();
    tabClickTrigger();

  });
  export default{
    name:'Resume',
    data(){
      return{
        intro:'广东云浮罗定人，2016年毕业于广东工业大学数字媒体技术专业，2015年5月开始实习，一直从事前端开发相关工作。' +
              '曾参与某国有银行网银系统内部开发，有p2p金融平台前端开发经验；' +
              '曾使用node.js+express+mongoDB独立开发某绿化公司宣传网站；' +
              '有微信公众号开发经验（对微信公众平台接口调用亦有所了解）。' +
              '熟练mv*开发模式（有vue.js开发经验），熟悉前端管理方案（了解gulp及webpack），熟悉node.js。' +
              '熟练Ps，Ai等设计软件的使用。'
      }
    }
  }
</script>
