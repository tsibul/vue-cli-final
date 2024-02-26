<template>
  <section class="news">
    <div class="projects__top">
      <div class="projects__top_title">Articles & News</div>
    </div>
    <div class="news__articles">
      <ArticleComponent v-for="(article, index) in articles.slice(0, 6)"
                        :key="index"
                        :article="article"
      />
    </div>
    <div class="news__articles_footer">
      <img src="@/assets/image/Pagination.png" alt="pgin">
    </div>

  </section>
</template>

<script>
import ArticleComponent from '@/components/articles/ArticleComponent.vue'

export default {
  name: 'BlogNewsComponent',
  components: { ArticleComponent },
  props: {
    articles: Array
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
    }
  }
}

.news {
  margin-top: 96px;

  &__articles {
    margin-top: 60px;
    display: grid;
    grid-template-columns: repeat(3, 382px);
    grid-template-rows: 1fr;
    overflow: hidden;
    justify-content: space-between;

    &_footer{
      display: flex;
      justify-content: center;
      margin-top: 52px;
      width: 100%;
    }
  }
}
</style>
