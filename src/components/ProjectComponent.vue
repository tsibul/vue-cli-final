<template>
  <div>
    <BlogBannerComponent />
    <div class="container">
      <LatestPostComponent/>
    </div>
    <div class="container">
      <BlogNewsComponent :articles="articleList"/>
    </div>
  </div>
</template>

<script>
import BlogBannerComponent from '@/components/blog/BlogBannerComponent.vue'
import LatestPostComponent from '@/components/blog/LatestPostComponent.vue'
import BlogNewsComponent from '@/components/blog/BlogNewsComponent.vue'
import articleList from '@/components/articles/articles'

export default {
  name: 'MainComponent',
  components: {
    BlogNewsComponent,
    LatestPostComponent,
    BlogBannerComponent
  },
  data () {
    return { articleList }
  },

  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
