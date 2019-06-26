<template>
  <div class="back-arrow" @tap="handleClick"></div>
</template>

<script>
export default {
  name: 'Back',
  props: {
    root: {
      type: Boolean,
      default: false
    }
  },
  methods: {
    handleClick() {
      this.$router.pop(this.root);
      this.$emit('click');
    }
  },
}
</script>

<style lang="postcss" scoped>
.back-arrow {
  width: 18px;
  height: 33px;
  background-image: url(./back-arrow@2x.png);
  background-size: 100% 100%;
  position: relative;
  &:after {
    position: absolute;
    content: '';
    top: -26px;
    bottom: -26px;
    left: -32px;
    right: -32px;
  }
}
</style>
