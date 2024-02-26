<template>
  <div id="app">
    <HeaderComponent @changeContent="changeContent" />
    <ContentComponent :componentType="componentType"/>
    <FooterComponent @changeContent="changeContent" />
  </div>
</template>

<script>
import HeaderComponent from '@/components/HeaderComponent.vue'
import FooterComponent from '@/components/FooterComponent.vue'
import ContentComponent from '@/components/ContentComponent.vue'

export default {
  name: 'App',
  components: {
    ContentComponent,
    HeaderComponent,
    FooterComponent
  },
  data () {
    return {
      componentType: 'MainComponent'
    }
  },
  methods: {
    changeContent (componentType) {
      this.componentType = componentType
    }
  }
}
</script>

<style lang="scss">
@import "assets/scss/vars";
@import "assets/scss/mixins";

@import url('https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&display=swap');

#app, menu {
  padding-inline-start: 0;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

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
    content: url("@/assets/icons/rightOrange.png");
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
      content: url("@/assets/icons/rightBlack.png");
    }

    &:hover {
      color: $colorPrimary;
    }
  }
}

</style>
