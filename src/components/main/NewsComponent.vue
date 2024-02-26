<template>
  <section class="news">
    <div class="projects__top">
      <div class="projects__top_title">Articles & News</div>
      <div class="projects__top_text">IIt is a long established fact that a reader will be distracted by the of
        readable content of a page when looking at its layouts the points of using.
      </div>
    </div>
    <div class="news__articles">
    </div>
  </section>
</template>

<script>
export default {
  name: 'NewsComponent',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/assets/scss/vars";
@import "@/assets/scss/mixins";

.projects {
  &__top {
    width: 737px;
    height: 137px;
    margin: 0 auto;

    &_title {
      padding: 8px 0;
      @include title();
      font-size: 50px;
      line-height: 62.5px;
      text-align: center;

      &_blog {
        text-align: start;
      }
    }

    &_text {
      @include text();
      font-size: 22px;
      line-height: 33px;
      text-align: center;
    }
  }
}

.news {
  margin-top: 96px;

  &__articles {
    margin-top: 60px;
    display: grid;
    grid-template-columns: repeat(3, 382px);
    justify-content: space-between;
  }
}
</style>
