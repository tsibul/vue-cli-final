<template>
  <section class="counter">
    <div class="counter__block">
      <div class="counter__block_item">
        <div class="counter__block_item-title">12</div>
        <div class="counter__block_item-text">Years Of Experience</div>
      </div>
      <img src="@/assets/image/Line.png" alt="line">
      <div class="counter__block_item">
        <div class="counter__block_item-title">85</div>
        <div class="counter__block_item-text">Success Project</div>
      </div>
      <img src="@/assets/image/Line.png" alt="line">
      <div class="counter__block_item">
        <div class="counter__block_item-title">15</div>
        <div class="counter__block_item-text">Active Project</div>
      </div>
      <img src="@/assets/image/Line.png" alt="line">
      <div class="counter__block_item">
        <div class="counter__block_item-title">95</div>
        <div class="counter__block_item-text">Happy Customers</div>
      </div>
    </div>
  </section></template>

<script>
export default {
  name: 'CounterComponent',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/assets/scss/vars";
@import "@/assets/scss/mixins";

.counter {
  margin-top: 96px;
  width: 100wv;
  background-color: #F4F0EC;
  height: 457px;
  display: flex;
  align-items: center;

  &__block {
    max-width: 1200px;
    margin: 0 auto;
    width: 100%;
    display: flex;
    justify-content: space-between;

    &_item {
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    &_item-title {
      @include title();
      padding: 16px 0 22px 0;
      font-size: 85px;
      line-height: 106.25px;
      color: $colorPrimary;
    }

    &_item-text {
      @include text();
      font-size: 22px;
      line-height: 33px;
    }
  }
}
</style>
