<template>
  <article class="article">
    <img :src="article.url" class="article__img" :alt="article.title">
    <div class="article__tag">{{ article.tag }}</div>
    <div class="article__title">{{ article.title }}</div>
    <div class="article__bottom">
      <div class="article__text">{{ article.date }}</div>
      <img src="@/assets/icons/next.svg" class="article__svg" alt="right">
    </div>
  </article>
</template>

<script>

export default {
  name: 'ArticleComponent',
  props: {
    article: Object,
    articleId: Number
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../../assets/scss/vars";
@import "../../assets/scss/mixins";

.article {
  padding: 21px;
  border: 1px solid #F4F0EC;
  border-radius: 60px;
  //height: 521px;
  position: relative;

  &:hover {
    background-color: #F4F0EC;
  }

  &:hover .article__svg {
    content: url('@/assets/icons/nextLight.svg');
  }

  &__img {
    border: 1px solid transparent;
    border-radius: 55px 55px 0 0;
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

  &__svg {
    height: 51px;
    width: 50px;
    cursor: pointer;
  }

  &__tag {
    border-radius: 8px 8px 8px 0;
    background-color: #fff;
    padding: 8px 10px;
    @include text;
    font-size: 16px;
    line-height: 24px;
    position: absolute;
    left: 44px;
    top: 252px;
  }

}
</style>
