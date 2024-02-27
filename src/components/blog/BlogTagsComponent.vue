<template>
  <div>
    <div class="details-tags__title">Tags</div>
    <div class="details-tags__btns">
      <span class="tags-span">
        <input type="radio" name="tags" checked id="tags-all" class="details-tags__btns_check">
        <label for="tags-all" class="tags-btn">All</label>
      </span>
      <BlogSingleTagComponent v-for="tag in tagList.tags" :key="tag.id" :tag="tag"/>
    </div>
  </div>
</template>

<script>

import articleList from '@/components/articles/articles'
import BlogSingleTagComponent from '@/components/blog/BlogSingleTagComponent.vue'

export default {
  name: 'BlogTagsComponent',
  props: {
    tags: Array
  },
  components: { BlogSingleTagComponent },
  methods: {
    showAll () {
      return { tagId: 0 }
    }
  },
  computed: {
    tagList () {
      return { tags: [...new Set(articleList.map(item => item.tag))] }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/assets/scss/vars";
@import "@/assets/scss/mixins";

.details-tags {
  &__title {
    @include title;
    font-size: 25px;
    line-height: 31.25px;
  }

  &__btns {
    margin-top: 24px;
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
    justify-content: flex-start;

    &_check {
      position: absolute;
      left: -999px;

      &:checked + label {
        color: #fff;
        background-color: $colorSecondary;
      }
    }
  }
}

.tags-btn {
  padding: 9px 30px;
  background-color: #F4F0EC;
  color: $colorSecondary;
  @include text;
  font-size: 18px;
  line-height: 22.5px;
  border: 1px solid transparent;
  border-radius: 10px;
  transition: background-color 0.2s, color 0.2s;
  cursor: pointer;

  &:hover {
    color: #fff;
    background-color: $colorSecondary;
  }

}

.tags-span {
  padding: 12px 0;
}
</style>
