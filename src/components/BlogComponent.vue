<template>
  <div>
    <div class="container">
      <BannerComponent/>
      <ProjectsComponent/>
    </div>
    <CounterComponent/>
    <div class="container">
    </div>
  </div>
</template>

<script>
import BannerComponent from '@/components/main/BannerComponent.vue'
import ProjectsComponent from '@/components/main/ProjectsComponent.vue'
import CounterComponent from '@/components/main/CounterComponent.vue'

export default {
  name: 'MainComponent',
  components: {
    CounterComponent,
    ProjectsComponent,
    BannerComponent
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
