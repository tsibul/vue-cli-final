<template>
  <div>
    <div class="container">
      <BannerComponent/>
      <ProjectsComponent :projects="projectsData"/>
    </div>
    <CounterComponent/>
    <div class="container">
      <NewsComponent/>
    </div>
  </div>
</template>

<script>
import BannerComponent from '@/components/main/BannerComponent.vue'
import ProjectsComponent from '@/components/main/ProjectsComponent.vue'
import CounterComponent from '@/components/main/CounterComponent.vue'
import NewsComponent from '@/components/main/NewsComponent.vue'
import projectsData from '@/components/main/projectsData'

export default {
  name: 'MainComponent',
  components: {
    NewsComponent,
    CounterComponent,
    ProjectsComponent,
    BannerComponent
  },
  data () {
    return { projectsData }
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
