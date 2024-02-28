<template>
  <section class="details_blog">
    <BlogTagsComponent @chosenTag="changeTag" />
    <BlogArticlesComponent :selectedTag="selectedTag" />
  </section>
</template>

<script>

import BlogTagsComponent from '@/components/blog/BlogTagsComponent.vue'
import BlogArticlesComponent from '@/components/blog/BlogArticlesComponent.vue'

export default {
  name: 'BlogDetailsComponent',
  data () {
    return { selectedTag: 'All' }
  },
  components: {
    BlogArticlesComponent,
    BlogTagsComponent
  },
  methods: {
    changeTag (selectedTag) {
      this.selectedTag = selectedTag
      console.log(selectedTag)
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
