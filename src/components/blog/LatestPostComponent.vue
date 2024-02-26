<template>
  <section class="latest-post">
    <div class="latest-post__title">Latest Post</div>
    <div class="latest-post__content">
      <img src="@/assets/image/lastPost.jpg" class="latest-post__content_img">
      <div class="latest-post__content_info">
        <div class="latest-post__content_title">Low Cost Latest Invented Interior Designing Ideas</div>
        <div class="latest-post__content_text">Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae
          turpis dignissim maximus.posuere in.Contrary to popular belief.
        </div>
        <div class="latest-post__content_text">Lorem Ipsum is not simply random text. It has roots in a piece of
          classic.
        </div>
        <div class="latest-post__content_bottom">
          <div class="news__articles_text">26 December,2022</div>
          <img src="@/assets/icons/next.svg" class="news__articles_svg" alt="right">
        </div>
      </div>
    </div>

  </section>
</template>

<script>
export default {
  name: 'LatestPostComponent',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/assets/scss/vars";
@import "@/assets/scss/mixins";

.latest-post {
  margin-top: 200px;
  display: flex;
  height: 612px;
  flex-direction: column;
  align-items: start;

  &__title {
    @include title;
    font-size: 50px;
    line-height: 62.5px;
    margin-bottom: 27px;
  }

  &__content {
    height: 522px;
    border: 1px solid #E7E7E7;
    border-radius: 60px;
    display: flex;
    justify-content: space-between;
    width: 100%;

    &_img {
      padding: 20px;
      border-radius: 55px;
      width: 569px;
    }

    &_info {
      padding: 24px;
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      justify-content: space-between;
      width: 489px;
    }

    &_title {
      @include title;
      font-size: 25px;
      line-height: 31.25px;

    }

    &_text {
      @include text;
      font-size: 22px;
      line-height: 33px;
    }

    &_bottom{
      display: flex;
      justify-content: space-between;
      align-items: center;
      width: 100%;
    }
  }
}
</style>
