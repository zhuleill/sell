<template>
  <span v-show="item.type>0" class="icon" :class="classMap[item.type]"></span>
</template>

<script type="text/ecmascript-6">
  export default {
    props: {
      item: {
        type: Object
      },
      size: {
        type: Number
      }
    },
    created() {
      this.classMap = ['decrease_' + this.size, 'discount_' + this.size, 'special_' + this.size, 'invoice_' +
      this.size, 'guarantee_' + this.size];
    }
  };
</script>

<style lang="stylus" rel="stylesheet/stylus">
  @import "../../common/stylus/mixin.styl"
  .goods
    .menu-wrapper
      .icon
        display: inline-block
        vertical-align: top
        width: 12px
        height: 12px
        margin-right: 2px
        background-size: 12px 12px
        background-repeat: no-repeat
        &.decrease_3
          bg-image('decrease_3')
        &.discount_3
          bg-image('discount_3')
        &.guarantee_3
          bg-image('guarantee_3')
        &.invoice_3
          bg-image('invoice_3')
        &.special_3
          bg-image('special_3')
</style>
