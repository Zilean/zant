<template>
  <i :class="classes" :style="styles"></i>
</template>

<script>
// zant 的图标使用开源项目 ionicons：http://ionicons.com/
const prefixCls = 'zant-icon';

export default {
  name: 'Icon',
  props: {
    type: String,
    size: [Number, String],
    color: String
  },
  computed: {
    classes () {
      return `${prefixCls} ${prefixCls}-${this.type}`;
    },
    styles () {
      let style = {};

      if (this.size) {
        style['font-size'] = `${this.size}px`;
      }

      if (this.color) {
        style.color = this.color;
      }

      return style;
    }
  }
}
</script>

