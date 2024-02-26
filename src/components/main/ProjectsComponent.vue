<template>
  <section class="projects">
    <div class="projects__top">
      <div class="projects__top_title">Follow Our Projects</div>
      <div class="projects__top_text">It is a long established fact that a reader will be distracted by
        the of readable content of page looking at its layouts points.
      </div>
    </div>
    <div class="projects__projects">
      <SingleProjectComponent
        v-for="(project, index) in projects"
        :key="index"
        :project="project"
        :corner-id="index % 4"
        :corner="corner"
      />
    </div>
  </section>
</template>

<script>
import SingleProjectComponent from '@/components/main/SingleProjectComponent.vue'

export default {
  name: 'ProjectsComponent',
  components: {
    SingleProjectComponent
  },
  props: {
    projects: Array
  },
  data () {
    return {
      corner: {
        0: 'rt',
        1: 'lt',
        2: 'rb',
        3: 'lb'
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../../assets/scss/vars";
@import "../../assets/scss/mixins";

.projects {
  margin-top: 96px;

  &__top {
    width: 737px;
    height: 137px;
    margin: 0 auto;

    &_title {
      padding: 8px 0;
      @include title;
      font-size: 50px;
      line-height: 62.5px;
      text-align: center;

      &_blog {
        text-align: start;
      }
    }

    &_text {
      @include text;
      font-size: 22px;
      line-height: 33px;
      text-align: center;
    }
  }

  &__projects {
    margin-top: 93px;
    display: grid;
    grid-template-columns: repeat(2, 525px);
    justify-content: space-between;
    gap: 56px;
  }
}
</style>
