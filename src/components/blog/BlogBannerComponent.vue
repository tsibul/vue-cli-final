<template>
  <section class="blog-banner">
    <div class="blog-banner__intro">
      <div class="blog-banner__title">Articles & News</div>
      <div class="blog-banner__text">Home / Blog</div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'BlogBannerComponent',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/assets/scss/vars";
@import "@/assets/scss/mixins";

.blog-banner {
  margin-top: 45px;
  width: 100%;
  height: 358px;
  background-image: url("@/assets/image/blogBanner.jpg");
  background-repeat: no-repeat;
  background-size: 100% 100%;
  display: flex;
  justify-content: center;
  align-items: end;

  &__intro {
    background-color: #fff;
    border: 1px solid transparent;
    border-radius: 55px 55px 0 0;
    padding: 41px 78px;
  }
  &__title {
    padding: 8px 0;
    @include title();
    font-size: 50px;
    line-height: 62.5px;
    text-align: center;
    &_blog{
      text-align: start;
    }
  }

  &__text {
    @include text();
    font-size: 22px;
    line-height: 33px;
    text-align: center;
  }

}
</style>
