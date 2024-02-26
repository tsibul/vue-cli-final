<template>
  <div>
    <div class="container">
      <ProjectsComponent/>
    </div>
    <CounterComponent/>
    <div class="container">
    </div>
  </div>
</template>

<script>
import ProjectsComponent from '@/components/main/ProjectsComponent.vue'
import CounterComponent from '@/components/main/CounterComponent.vue'

export default {
  name: 'MainComponent',
  components: {
    CounterComponent,
    ProjectsComponent
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
