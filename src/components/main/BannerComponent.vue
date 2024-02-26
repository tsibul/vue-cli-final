<template>
  <section class="banner">
    <img src="@/assets/image/livingRoom.jpg" class="banner-image" alt="living room">
    <div class="banner__subcontent">
      <div class="banner__subcontent_title">Let Your Home
        Be Unique
      </div>
      <div class="banner__subcontent_title_text">There are many variations of the passages of
        lorem Ipsum from available, majority.
      </div>
      <button type="button" class="btn">Get Started</button>
    </div>
  </section>
</template>

<script>
export default {
  name: 'BannerComponent',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/assets/scss/vars";
@import "@/assets/scss/mixins";

.banner {
  margin-top: 57px;
  height: 758px;
  display: flex;
  align-items: center;
  justify-content: start;
  position: relative;
  z-index: 2;
  background-color: #fff;

  &__subcontent {
    position: absolute;
    padding-left: 72px;
    display: flex;
    flex-direction: column;
    align-items: start;
    gap: 20px;
    width: 506px;

    &_title {
      @include title();
      padding-top: 8px;
      font-size: 65px;
      line-height: 81.25px;

      &_text {
        @include text();
        font-size: 22px;
        line-height: 33px;
      }
    }

  }
}

.banner-image {
  @include roundAll();
}
</style>
