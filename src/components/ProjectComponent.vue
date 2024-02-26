<template>
  <div>
    <ProjectBannerComponent />
    <div class="container">
      <LatestPostComponent/>
    </div>
    <div class="container">
      <ProjectNewsComponent :articles="articleList"/>
    </div>
  </div>
</template>

<script>
import ProjectBannerComponent from '@/components/project/ProjectBannerComponent.vue'
import LatestPostComponent from '@/components/project/LatestPostComponent.vue'
import ProjectNewsComponent from '@/components/project/ProjectNewsComponent.vue'
import articleList from '@/components/articles/articles'

export default {
  name: 'MainComponent',
  components: {
    ProjectNewsComponent,
    LatestPostComponent,
    ProjectBannerComponent
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
