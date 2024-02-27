<template>
  <div class="details-layout">
    <CurrentPostComponent :article-id="articleId"/>  </div>
</template>

<script>
import CurrentPostComponent from '@/components/blog/CurrentPostComponent.vue'

export default {
  name: 'BlogLayoutComponent',
  components: {
    CurrentPostComponent
  },
  data () {
    return {
      articleId: 6
    }
  },
  methods: {
    changeContent (id) {
      this.articleId = id
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
