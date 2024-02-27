<template>
  <section class="current-post">
    <div class="current-post__title">{{ currentArticle.title }}</div>
    <img :src="currentArticle.url" alt="pict1" class="current-post__img1">
    <div class="current-post__details">
      <div class="current-post__small">{{ currentArticle.date }}</div>
      <div class="current-post__small">Interior&nbsp;/&nbsp;Home&nbsp;/&nbsp;{{ currentArticle.tag }}</div>
    </div>
    <div class="current-post__text" v-html="currentArticle.summary"></div>
    <div class="current-post__banner">
      <img src="@/assets/image/kocki.png" alt="kocki">
      <div class="current-post__banner_it">The details are not the details.
        They make the design.
      </div>
    </div>
    <div class="current-post__title">{{ currentArticle.contentTitle }}</div>
    <div class="current-post__text">{{ currentArticle.contentIntro }}</div>
    <div class="current-post__text" v-for="(item, index) in currentArticle.content"
         :key="index"
    >{{ item }}
    </div>
    <img :src="currentArticle.url2" alt="pict2" class="current-post__img2">
    <div class="current-post__text">{{ currentArticle.conclusion }}</div>
  </section>

</template>

<script>
import articleList from '@/components/articles/articles'

export default {
  name: 'CurrentPostComponent',
  props: {
    currentArticle: {
      type: Object,
      default: function () {
        return articleList[this.articleId || 6]
      }
    },
    articleId: {
      type: Number,
      default: 6
    }
  },
  data () {
    return { articleList }
  },
  // methods: {
  //   getArticle (articleId) {
  //     return articleList[articleId]
  //   }
  // },
  created () {
    if (!this.currentArticle) {
      this.$emit('update:currentArticle', articleList[this.articleId])
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/assets/scss/vars";
@import "@/assets/scss/mixins";

.current-post {
  &__title {
    @include title;
    font-size: 50px;
    line-height: 62.5px;
  }

  &__text {
    margin-top: 36px;
    @include text;
    font-size: 22px;
    line-height: 33px;
  }

  &__details {
    margin-top: 24px;
    display: flex;
    justify-content: space-between;
    padding-right: 36px;
  }

  &__banner {
    margin: 24px 0;
    height: 287px;
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: #F4F0EC;
    border-radius: 70px;
    justify-content: center;

    &_it {
      margin-top: 10px;
      @include title;
      font-size: 25px;
      font-style: italic;
      width: 345px;
      color: $colorPrimary;
      text-align: center;
    }
  }

  &__small {
    @include text;
    font-size: 16px;
    line-height: 24px;
  }

  &__img1 {
    margin: 16px 0 24px 0;
    border-radius: 70px;
    width: 100%;
  }

  &__img2 {
    margin: 24px 0 0 0;
    border-radius: 70px;
    width: 100%;
  }
}

</style>
