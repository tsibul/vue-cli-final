<template>
<span class="tags-span" @click="emitTag">
  <input type="radio" name="tags" :id="'tags-'+ tag.replace(' ', '_')"
         class="tags-btn__check">
  <label :for="'tags-'+ tag.replace(' ', '_')" class="tags-btn">{{ tag }}</label>
</span>
</template>

<script>

export default {
  name: 'BlogSingleTagComponent',
  props: {
    tag: String
  },
  methods: {
    emitTag () {
      this.$emit('chosenTag', this.tag)
    }
  },
  components: {}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/assets/scss/vars";
@import "@/assets/scss/mixins";

.tags-span {
  padding: 12px 0;
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

  &__check {
    position: absolute;
    left: -999px;
    &:checked + label {
      color: #fff;
      background-color: $colorSecondary;
    }

  }
}

</style>
