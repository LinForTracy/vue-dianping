<template>
  <div class="star-wrap">
    <i class="iconfont icon-star" :class="{active: item <= score}" v-for="item in [0, 1, 2, 3, 4]" :key="item"></i>
  </div>
</template>

<script>
export default {
  name: 'Star',
  props: {
    score: {
      type: Number,
      default: 0
    }
  }
};
</script>

<style lang="scss" scoped>
.star-wrap {
  @include frow(flex-start);
  .icon-star {
    font-size: 18px;
    color: $fs999;
    &.active {
      color: $fsf33;
    }
  }
}
</style>
