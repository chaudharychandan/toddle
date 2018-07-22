<template>
  <div v-bind:class="{'pb-4': size === 'lg'}" class="t-headline">
    <h2 v-if="size === 'lg'" class="headline mb-2">{{ title }}</h2>
    <h5 v-if="size !== 'lg'" class="subheading mb-2">{{ title }}</h5>
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
  .headline, .subheading {
    font-weight: 600;
    color: inherit;
  }
}
</style>
