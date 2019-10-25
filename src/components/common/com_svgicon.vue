<!--
 * @Author: yongwei.hou
 * @Date: 2019-10-25 15:46:19
 * @LastEditors: yongwei.hou
 * @LastEditTime: 2019-10-25 16:24:07
 * @Description:
 -->
<template>
  <svg :class="svgClass" aria-hidden="true">
    <use :href="iconName"></use>
  </svg>
</template>

<script>
export default {
  name: "SvgIcon",
  props: {
    iconClass: {
      type: String,
      required: true
    },
    className: {
      type: String,
      default: ""
    }
  },
  computed: {
    iconName() {
      return `#icon-${this.iconClass}`;
    },
    svgClass() {
      if (this.className) {
        return "svg-icon " + this.className;
      } else {
        return "svg-icon";
      }
    }
  }
};
</script>

<style scoped>
.svg-icon {
  vertical-align: -0.15em;
  fill: currentColor;
  overflow: hidden;
}
</style>
