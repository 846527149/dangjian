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
      <div @click="playPause" class="menu_button">
        <svg-icon icon-class="playbutton" class="play_menu"/>
      </div>
      <video id="video1">
        <source src="https://www.w3school.com.cn/example/html5/mov_bbb.mp4" type="video/mp4">
      </video>
    </div>
    <div class="index_menu">
      <div class="index_menu_row">
        <div class="index_menu_col">
          <a class="col_box">
            <svg-icon icon-class="党务公开" class="menu_icon"/>
            <span>党务公开</span>
          </a>
        </div>
        <div class="index_menu_col">
          <a class="col_box">
            <svg-icon icon-class="党务公开" class="menu_icon"/>
            <span>党务公开</span>
          </a>
        </div>
        <div class="index_menu_col">
          <a class="col_box">
            <svg-icon icon-class="党务公开" class="menu_icon"/>
            <span>党务公开</span>
          </a>
        </div>
        <div class="index_menu_col">
          <a class="col_box">
            <svg-icon icon-class="党务公开" class="menu_icon"/>
            <span>党务公开</span>
          </a>
        </div>
        <div class="index_menu_col">
          <a class="col_box">
            <svg-icon icon-class="党务公开" class="menu_icon"/>
            <span>党务公开</span>
          </a>
        </div>
        <div class="index_menu_col">
          <a class="col_box">
            <svg-icon icon-class="党务公开" class="menu_icon"/>
            <span>党务公开</span>
          </a>
        </div>
      </div>
    </div>
    <div class="index_subject">
      <img src="../assets/images/专题banner.jpg">
    </div>
    <div class="index_system">
      <ul>
        <li>民主评议党员制度</li>
        <li>民主评议党员制度</li>
        <li>民主评议党员制度</li>
        <li>民主评议党员制度</li>
        <li>民主评议党员制度</li>
        <li>民主评议党员制度</li>
        <li>民主评议党员制度</li>
        <li>民主评议党员制度</li>
        <li>民主评议党员制度</li>
      </ul>
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
.play_menu {
}
.index_system ul li {
  float: left;
  width: 33.3%;
}
.index_video {
  .menu_button {
    position: absolute;
    left: 50%;
  }
}
.index_menu_row {
  display: flex;
  display: -webkit-flex;
}
.index_menu_row .index_menu_col {
  width: 1.6rem;
  .col_box {
    text-align: center;
    display: block;
    float: left;
    .menu_icon {
      width: 1rem;
      height: 1rem;
    }
    span {
      display: block;
      margin-top: 0.3rem;
      .font-dpr(12px);
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
