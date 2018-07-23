<template>
  <v-flex class="white py-4 elevation-1">
    <v-layout row align-start px-3>
      <v-icon color="cyan">assignment</v-icon>
      <base-headline
        title="Your Activity"
        description="Catch the recap of your activities and road maphere along with time stamp"
        size="md"
        class="ml-2"
      >
      </base-headline>
    </v-layout>
    <activities v-bind:items="activities" class="my-2"></activities>
  </v-flex>
</template>

<script>
import Activities from '@/components/Activities.vue';

export default {
  name: 'ActivityMap',
  components: {
    activities: Activities,
  },
  props: {
    activities: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style scoped lang="scss">

</style>
