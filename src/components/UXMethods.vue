<template>
  <v-layout column>
    <v-layout row justify-space-between align-center pb-5>
      <base-headline
        title="UX Methods"
        size="md"
      >
      </base-headline>
    </v-layout>
    <v-container fluid align-center grid-list-lg pa-0>
      <v-layout row wrap>
        <v-flex xl2 lg3 sm4 xs12 v-for="item in items" v-bind:key="item.id">
          <ux-method-card v-bind:method="item"></ux-method-card>
        </v-flex>
      </v-layout>
    </v-container>
  </v-layout>
</template>

<script>
import UXMethodCard from '@/components/UXMethodCard.vue';

export default {
  name: 'UXMethods',
  components: {
    'ux-method-card': UXMethodCard,
  },
  props: {
    items: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style lang="scss">

</style>
