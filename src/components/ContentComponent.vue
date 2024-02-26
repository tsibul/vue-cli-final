<template>
  <component :is="componentType" />
</template>

<script>

import MainComponent from '@/components/MainComponent.vue'
import BlogComponent from '@/components/BlogComponent.vue'
import ProjectComponent from '@/components/ProjectComponent.vue'

export default {
  name: 'ContentComponent',
  props: {
    componentType: {
      type: String,
      required: true
    }
  },
  components: {
    MainComponent,
    ProjectComponent,
    BlogComponent
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/scss/vars";
@import "../assets/scss/mixins";

.btn {
  padding: 25px 77px 25px 53px;
  color: #fff;
  background-color: $colorSecondary;
  font-family: Jost, sans-serif;
  font-size: 18px;
  font-weight: 600;
  line-height: 22.5px;
  letter-spacing: 0.02em;
  text-align: center;
  position: relative;
  border: 1px solid $colorSecondary;
  border-radius: 18px;
  transition: background-color 0.2s, color 0.2s;

  &:after {
    content: url("../assets/icons/rightOrange.png");
    position: absolute;
    top: calc(50%);
    right: 53px;
    transform: translateY(-50%);

  }

  &:hover {
    color: $colorSecondary;
    background-color: transparent;
  }

  &__color {
    background-color: $colorPrimary;
    border-color: $colorPrimary;

    &:after {
      content: url("../assets/icons/rightBlack.png");
    }

    &:hover {
      color: $colorPrimary;
    }
  }
}

</style>
