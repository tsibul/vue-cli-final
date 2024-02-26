<template>
  <article class="article__item">
    <img :src="article.url" class="article__img" alt="article image">
    <div class="article__tag">{{ article.tag }}</div>
    <div class="article__title">{{ article.title}}</div>
    <div class="articles__bottom">
      <div class="articles__text">{{ article.date}}</div>
      <img src="@/assets/icons/next.svg" class="articles__svg" alt="right">
    </div>
  </article>
</template>

<script>

export default {
  name: 'ArticleComponent',
  props: {
    article: Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/assets/scss/vars";
@import "@/assets/scss/mixins";

.article {
  margin-top: 60px;
  display: grid;
  grid-template-columns: repeat(3, 382px);
  justify-content: space-between;

  &__item {
    padding: 21px;
    border: 1px solid #F4F0EC;
    border-radius: 60px;
    height: 521px;
    position: relative;
  }

  &__img {
    border: 1px solid transparent;
    border-radius: 55px 55px 0 0;
    //height: 289px;
    //object-fit: fill;
    width: 100%;
    aspect-ratio: 34 / 29;
  }

  &__title {
    margin-top: 6px;
    @include title;
    width: 80%;
    font-size: 25px;
    line-height: 31.25px;
    text-align: start;
  }

  &__bottom {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  &__text {
    margin-top: 30px;
    @include text;
    font-size: 16px;
    line-height: 24px;
    height: 52px;
    z-index: 2;
  }
}
</style>
