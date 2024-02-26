<template>
  <div class="container">
    <header class="menu">
      <menu class="menu__left" @click="changeContent('MainComponent')">
        <img src="@/assets/icons/Logo.png" height="34" alt="Logo">
        <div class="menu__title">Interno</div>
      </menu>
      <menu class="menu__right">
        <div class="menu__item" @click="changeContent('MainComponent')">Home</div>
        <div class="menu__item" @click="changeContent('ProjectComponent')">Project</div>
        <div class="menu__item" @click="changeContent('BlogComponent')">Blog</div>
      </menu>
    </header>
  </div>
</template>

<script>
export default {
  name: 'HeaderComponent',
  methods: {
    changeContent (componentType) {
      this.$emit('changeContent', componentType)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/assets/scss/vars";
@import "@/assets/scss/mixins";

.menu {
  display: flex;
  justify-content: space-between;
  margin-top: 44px;
  align-items: center;
  height: 50px;

  &__left {
    display: flex;
    justify-content: flex-start;
    gap: 10px;
    align-items: center;
    cursor: pointer;
  }

  &__right {
    display: flex;
    justify-content: space-between;
    width: 243px;
  }

  &__title {
    @include title;
    font-size: 40px;
    line-height: 50px;

    &:hover {
      color: $colorPrimary;
    }
  }

  &__item {
    @include text;
    font-size: 20px;
    line-height: 25px;
    text-align: center;
    height: 100%;
    cursor: pointer;

    &:hover {
      color: $colorPrimary;
    }
  }
}
</style>
