<template>
  <div v-bind:class="{'pb-4': size === 'lg'}" class="t-headline">
    <h2 v-if="size === 'lg'" class="headline mb-2">{{ title }}</h2>
    <h3 v-else-if="size === 'md'" class="title mb-2">{{ title }}</h3>
    <h4 v-else-if="size === 'sm'" class="subheading mb-2">{{ title }}</h4>
    <h5 v-else-if="size === 'xs'" class="body-2 mb-2">{{ title }}</h5>
    <h4 v-else class="subheading mb-2">{{ title }}</h4>
    <span class="grey--text">{{ description }}</span>
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
