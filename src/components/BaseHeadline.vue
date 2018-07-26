<template>
  <div
    v-bind:class="{'pb-4': size === 'lg'}"
    class="t-headline"
    v-bind:style="{color: tColor, height : height + 'px'}">
    <h2 v-if="size === 'lg'" class="headline">{{ title }}</h2>
    <h3 v-else-if="size === 'md'" class="title">{{ title }}</h3>
    <h4 v-else-if="size === 'sm'" class="subheading">{{ title }}</h4>
    <h5 v-else-if="size === 'xs'" class="body-2">{{ title }}</h5>
    <h4 v-else class="subheading">{{ title }}</h4>
    <div class="grey--text mt-2" v-if="description">
      <span v-bind:style="{ color: dColor }">
        {{ description }}
      </span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Headline',
  props: {
    title: {
      type: String,
      required: true,
    },
    size: String,
    description: String,
    height: String || Number,
    tColor: String,
    dColor: String,
  },
};
</script>

<style scoped lang="scss">
.t-headline{
  .headline, .title, .subheading, .body-2 {
    font-weight: 600;
    color: inherit;
  }
}
</style>
