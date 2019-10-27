<!--
 * @Author: yongwei.hou
 * @LastEditors: yongwei.hou
 * @Description: 首页
 * @Date: 2019-02-22 17:37:39
 * @LastEditTime: 2019-10-25 17:23:41
 -->

<template>
  <div>
    <div class="index_video">
       <img src="../assets/images/cache.jpg">
    </div>
    <div class="index_menu">
      <div class="menu_bg_l"></div>
      <div class="index_menu_row">
        <div class="index_menu_col">
          <a class="col_box">
            <svg-icon icon-class="dangwugongkai" class="menu_icon" />
            <span>党务公开</span>
          </a>
        </div>
        <div class="index_menu_col">
          <a class="col_box">
            <svg-icon icon-class="zuzhijiagou" class="menu_icon" />
            <span>组织架构</span>
          </a>
        </div>
        <div class="index_menu_col">
          <a class="col_box">
            <svg-icon icon-class="zhibujieshao" class="menu_icon" />
            <span>支部介绍</span>
          </a>
        </div>
        <div class="index_menu_col">
          <a class="col_box">
            <svg-icon icon-class="dangyuanfengcai" class="menu_icon" />
            <span>党员风采</span>
          </a>
        </div>
        <div class="index_menu_col">
          <a class="col_box">
            <svg-icon icon-class="rudangshici" class="menu_icon" />
            <span>入党誓词</span>
          </a>
        </div>
        <div class="index_menu_col">
          <a class="col_box">
            <svg-icon icon-class="huanyingmoshi" class="menu_icon" />
            <span>欢迎模式</span>
          </a>
        </div>
      </div>
      <div class="menu_bg_r"></div>
    </div>
    <div class="index_subject">
      <img src="../assets/images/专题banner.jpg">
    </div>
    <div class="index_system">
      <div class="menu_bg_l"></div>
      <ul class="system_ul">
        <li>民主评议党员制度</li>
        <li>党支部换届选举</li>
        <li>党员组织关系转接</li>
        <li>党的组织生活制度</li>
        <li>党员的学习制度</li>
        <li>党费收缴管理制度</li>
        <li>党章党规制度制度</li>
        <li>发展党员的流程</li>
        <li>党风廉政制度建设</li>
      </ul>
      <div class="menu_bg_r"></div>
    </div>
  </div>
</template>

<script>
import menuData from "../../src/data/data_menu.json";
export default {
  components: {},
  data() {
    return {
      menuList: null
    };
  },
  mounted() {
    this.setMenuData();
  },
  methods: {
    // 首页菜单赋值
    setMenuData() {
      this.menuList = menuData.menu;
    },
    playPause() {
      var myVideo = document.getElementById("video1");

      if (myVideo.paused) myVideo.play();
      else myVideo.pause();
    }
  }
};
</script>
<style lang="less" scoped>
@import url("../assets/less/_mixins/_mixins.less");
ul {
  list-style: none;
  margin: 0px;
  padding: 0px;
  width: auto;
}
.index_video {
  img{
    width: 100%;
  }
}
.menu_bg_l {
  width: 0.1067rem;
  background: #ff0000;
  height: 100%;
}
.menu_bg_r {
  width: 0.1067rem;
  background: #ff0000;
  height: 100%;
}
.index_menu {
  margin-bottom: 0.6667rem;
  margin-top: 0.6667rem;
  height: 2.4rem;
  display: flex;
}
.index_system {
  height: 2.1333rem;
  display: flex;
  margin-top: 0.6667rem;
  .system_ul{
    padding-left: 0.2667rem;
    color:#990000;
  }
}

.index_system ul li {
  float: left;
  width: 33.3%;
  line-height: 2;
}
.index_video {
  .menu_button {
    position: absolute;
    left: 50%;
  }
}
.index_menu_row {
  margin-top: 0.2667rem;
  display: flex;
  display: -webkit-flex;
      width: 100%;
}
.index_menu_row .index_menu_col {
  width: 1.6rem;
  .col_box {
    text-align: center;
    display: block;
    .menu_icon {
      width: 1rem;
      height: 1rem;
    }
    span {
      display: block;
      margin-top: 0.2rem;
      .font-dpr(10px);
      color: #666;
    }
  }
}
.index_subject {
  img {
    width: 100%;
  }
}
</style>
