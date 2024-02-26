<template>
  <div class="project-item">
    <img :src="project.url" :class="`project-item__${corner[cornerId]}`" :alt="project.title">
    <div class="project-item__footer">
      <div class="project-item__info">
        <div class="project-item__title">{{ project.title }}</div>
        <div class="project-item__text">{{ project.text }}</div>
      </div>
      <img src="@/assets/icons/next.svg" alt="next">
    </div>
  </div>
</template>

<script>

export default {
  name: 'SingleProjectComponent',
  props: {
    project: Object,
    cornerId: Number,
    corner: Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../../assets/scss/vars";
@import "../../assets/scss/mixins";

.project-item {
  width: 525px;

  &__footer {
    width: 100%;
    margin-top: 24px;
    display: flex;
    justify-content: space-between;
  }

  &__info {
    display: flex;
    align-items: start;
    flex-direction: column;
  }

  &__title {
    @include title();
    font-size: 25px;
    line-height: 31.25px;
  }

  &__text {
    @include text();
    font-size: 22px;
    line-height: 30px;
  }

  &__rt {
    width: 525px;
    @include roundRT;
  }

  &__lt {
    width: 525px;
    @include roundLT;
  }

  &__rb {
    width: 525px;
    @include roundRB;
  }

  &__lb {
    width: 525px;
    @include roundLB;
  }
}

</style>
