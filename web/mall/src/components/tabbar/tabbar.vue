<template>
  <div class="weui_tabbar">
    <slot></slot>
  </div>
</template>

<script>
import { parentMixin } from '../../libs/components/mixins/multi-items'

export default {
  mixins: [parentMixin],
  props: {
    iconClass: String
  }
}
</script>

<style lang="less">
@import '../../assets/styles/components/weui/widget/weui_tab/weui_tab_tabbar.less';
@import '../../assets/styles/components/reddot.less';

.weui_tabbar_icon {
  position: relative;
}
.weui_tabbar_icon > sup {
  position: absolute;
  top: -8px;
  left: 100%;
  transform: translateX(-50%);
  z-index: 101;
}
.weui_tabbar_item.vux-tabbar-simple {
  padding: 0;
  height: 50px;
  line-height: 50px;
}
.vux-tabbar-simple .weui_tabbar_label {
  font-size: 14px;
}
</style>
