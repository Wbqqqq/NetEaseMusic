<template>
  <div class="header">
    <!--注意点: 不能直接插槽设置样式-->
    <div class="left">
      <slot name="left">左边</slot>
    </div>
    <slot name="center">中间</slot>
    <div class="right">
      <slot name="right">右边</slot>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
  data () {
    return {

    }
  },
  methods: {

  }
}
</script>

<style scoped lang="scss">
  @import "../assets/css/variable";
  @import "../assets/css/mixin";
  .header{
    width: 100%;
    height: 100px;
    @include bg_color();
    display: flex;
    justify-content: space-between;
    .left, .right{
      width: 84px;
      height: 84px;
      margin-top: 8px;
      *{
        width: 100%;
        height: 100%;
      }
    }
  }
</style>
