<template>
  <v-layout column>
    <v-layout row justify-space-between align-center pb-5>
      <h3>UX Methods</h3>
      <div>
        <base-select
          v-bind:list="selections"
          v-bind:default="selected"
          v-on:change="selectType"
        >
        </base-select>
      </div>
    </v-layout>
    <v-container fluid align-center grid-list-lg pa-0>
      <v-layout row wrap>
        <v-flex sm3 v-for="item in filterMethods" v-bind:key="item.id">
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
  methods: {
    selectType(type) {
      this.selected = type;
    },
  },
  data() {
    return {
      selections: [
        {
          label: 'All',
          value: 0,
        },
        {
          label: 'New',
          value: 1,
        },
        {
          label: 'Popular',
          value: 2,
        },
      ],
      selected: 2,
    };
  },
  computed: {
    filterMethods() {
      return this.selected ? this.items.filter(item => item.type === this.selected) : this.items;
    },
  },
};
</script>

<style lang="scss">

</style>
