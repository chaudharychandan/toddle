<template>
  <v-card>
    <v-card-media
      :src="`https://unsplash.it/150/300?image=${Math.floor(Math.random() * 100) + 1}`"
      height="150"
    ></v-card-media>
    <v-card-title primary-title>
      <base-headline
        v-bind:title="project.title"
        v-bind:description="project.description"
      >
      </base-headline>
    </v-card-title>
  </v-card>
</template>

<script>
export default {
  name: 'ProjectCard',
  props: {
    project: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style lang="scss" scoped>
</style>
