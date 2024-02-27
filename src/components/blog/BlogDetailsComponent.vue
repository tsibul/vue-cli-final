<template>
  <section class="details_blog">
    <BlogTagsComponent/>
    <BlogArticlesComponent/>
  </section>
</template>

<script>

import BlogTagsComponent from '@/components/blog/BlogTagsComponent.vue'
import BlogArticlesComponent from '@/components/blog/BlogArticlesComponent.vue'

export default {
  name: 'BlogDetailsComponent',
  components: {
    BlogArticlesComponent,
    BlogTagsComponent
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
