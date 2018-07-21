<template>
  <div class="pb-4">
    <h3 class="headline mb-2">{{ title }}</h3>
    <span class="grey--text">{{ description }}</span>
  </div>
</template>

<script>
export default {
  name: 'Subheader',
  props: {
    title: {
      type: String,
      required: true,
    },
    description: String,
  },
};
</script>

<style scoped lang="scss">
  .headline {
    font-weight: 600;
  }
</style>
