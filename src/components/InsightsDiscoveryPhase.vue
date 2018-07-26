<template>
  <v-layout column>
    <v-layout row justify-space-between align-center pb-5>
      <base-headline
        title="Insights: Discovery Phase"
        description="Lorem inpsum dolor sit amet, consectetur."
        size="md"
      >
      </base-headline>
    </v-layout>
    <v-container fluid align-center grid-list-lg pa-0>
      <v-layout row wrap>
        <v-flex xl2 lg3 sm4 xs12 v-for="item in items" v-bind:key="item.id">
          <base-card
            v-bind:actions="actions"
            v-bind:card="item"
            color="#6EA7B8"
            title-text-color="white"
            description-text-color="white"
          >
          </base-card>
        </v-flex>
      </v-layout>
    </v-container>
  </v-layout>
</template>

<script>

export default {
  name: 'InsightsDiscoveryPhase',
  components: {
  },
  props: {
    items: {
      type: Array,
      required: true,
      default: () => [],
    },
  },
  data() {
    return {
      actions: [
        {
          label: 'Download',
          callback: (step) => {
            this.download(step);
          },
        },
        {
          label: 'Share',
          callback: (step) => {
            this.share(step);
          },
        },
      ],
    };
  },
  methods: {
    download(step) {
      console.log(step);
    },
    share(step) {
      console.log(step);
    },
  },
};
</script>

<style lang="scss">

</style>
