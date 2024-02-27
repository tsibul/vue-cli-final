<template>
  <div>
    <section class="details-first"></section>
    <div class="container">
 <BlogLayoutComponent/>
    </div>
  </div>
</template>

<script>

import BlogLayoutComponent from '@/components/blog/BlogLayoutComponent.vue'

export default {
  name: 'BlogComponent',
  components: {
    BlogLayoutComponent
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/assets/scss/vars";
@import "@/assets/scss/mixins";

.details-first {
  max-width: 2500px;
  margin: 45px auto 0;
  width: 100%;
  height: 351px;
  background-image: url("@/assets/image/blogDetailBanner.jpg");
  background-repeat: no-repeat;
  background-size: 100% 100%;
}
</style>
