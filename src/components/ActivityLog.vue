<template>
  <v-layout row my-3>
    <v-flex md2>
    </v-flex>
    <v-layout column>
      <div class="grey--text pb-2">{{ getTime }}</div>
      <base-headline
        v-bind:title="activity.title"
        v-bind:description="activity.description"
        size="xs"
      >
      </base-headline>
      <v-flex py-1>
        <v-layout row wrap>
          <v-chip
            v-for="item in activity.types"
            v-bind:key="item"
            label
            color="grey lighten-3"
            small
          >
            {{ item }}
          </v-chip>
        </v-layout>
      </v-flex>
    </v-layout>
  </v-layout>
</template>

<script>
export default {
  name: 'Activity',
  props: {
    activity: {
      type: Object,
      required: true,
    },
  },
  computed: {
    getTime() {
      return new Date(this.activity.timestamp).toDateString();
    },
  },
};
</script>

<style scoped lang="scss">
</style>
