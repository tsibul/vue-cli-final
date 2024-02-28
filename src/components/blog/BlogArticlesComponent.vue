<template>
  <section class="details_blog">
    <ArticleComponent v-for="(article, index) in tagFilterArticles"
                      :key="index"
                      :article="article"/>
  </section>
</template>

<script>

import ArticleComponent from '@/components/articles/ArticleComponent.vue'
import articleList from '@/components/articles/articles'

export default {
  name: 'BlogArticlesComponent',
  props: {
    selectedTag: String
  },
  components: { ArticleComponent },
  computed: {
    tagFilterArticles: function () {
      if (this.selectedTag === 'All') {
        return articleList
      } else {
        return Array.from(articleList.filter(a => a.tag === this.selectedTag))
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/assets/scss/vars";
@import "@/assets/scss/mixins";

.details-layout {
  margin-top: 200px;
  display: grid;
  grid-template-columns: 804px 345px;
  justify-content: space-between;
}
</style>
