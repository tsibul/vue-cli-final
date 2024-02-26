<template>
  <div class="container">
    <footer class="footer">
      <div class="footer__left">
        <div class="menu__left" @click="changeContent('MainComponent')">
          <img src="@/assets/icons/Logo.png" height="34" alt="logo">
          <div class="menu__title">Interno</div>
        </div>
        <div class="footer__text">It is a long established fact that a reader will be distracted looking.</div>
        <div class="footer__social">
          <img src="@/assets/icons/tw.svg" alt="twitter">
          <img src="@/assets/icons/inst.svg" alt="instagram">
        </div>
      </div>

      <div class="footer__middle">
        <div class="footer__title">Pages</div>
        <div class="footer__text footer__text_link" @click="changeContent('MainComponent')">Home</div>
        <div class="footer__text footer__text_link" @click="changeContent('ProjectComponent')">Project</div>
        <div class="footer__text footer__text_link" @click="changeContent('BlogComponent')">Blog</div>
      </div>
      <div class="footer__middle"></div>
      <div class="footer__right">
        <div class="footer__title">Contact</div>
        <div class="footer__text">55 East Birchwood Ave. Brooklyn, New York 11201</div>
        <div class="footer__text">contact@interno.com</div>
        <div class="footer__text">(123) 456 - 7890</div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'FooterComponent',
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

.footer{
  margin-top: 96px;
  height: 406px;
  display: flex;
  justify-content: space-between;

  &__left{
    display: flex;
    flex-direction: column;
    align-items: start;
    width: 393px;
    gap: 26px;

  }
  &__middle{
    display: flex;
    flex-direction: column;
    gap: 26px;
    align-items: start;
    width: 122px;
  }
  &__right{
    display: flex;
    flex-direction: column;
    gap: 26px;
    align-items: start;
    width: 256px;
  }

  &__text{
    @include text;
    font-size: 22px;
    line-height: 33px;

    &:hover{
      color: $colorPrimary;
    }
    &_link{
      cursor: pointer;
    }
  }
  &__title{
    @include title;
    font-size: 25px;
    line-height: 31.25px;
  }

  &__social{
    display: flex;
    gap: 54px;
    justify-content: start;
  }
}

.menu {
  &__left {
    display: flex;
    justify-content: start;
    gap: 10px;
    align-items: center;
    cursor: pointer;
  }
  &__title {
    @include title;
    font-size: 40px;
    line-height: 50px;

    &:hover {
      color: $colorPrimary;
    }
  }
}
</style>
