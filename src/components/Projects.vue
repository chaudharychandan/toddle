<template>
  <v-layout column>
    <v-layout row justify-space-between align-center>
      <base-headline
        title="Your Projects"
        size="md"
      >
      </base-headline>
      <div>
        <v-layout row align-center>
          <v-flex>
            <base-select
              v-bind:list="selections"
              v-bind:default="selected"
              v-on:change="selectStatus"
            >
            </base-select>
          </v-flex>
          <v-flex hidden-sm-and-down>
            <v-btn color="primary">
              <v-icon left dark>add</v-icon>
              Start New Project
            </v-btn>
          </v-flex>
        </v-layout>
      </div>
    </v-layout>
    <v-divider class="my-4"></v-divider>
    <v-container fluid align-center grid-list-lg pa-0>
      <v-layout row wrap>
        <v-flex xl2 lg3 sm4 xs12 v-for="item in filterProjects" v-bind:key="item.id">
          <router-link :to="{ name: 'project', params: { name: item.title }}">
            <project-card v-bind:project="item"></project-card>
          </router-link>
        </v-flex>
      </v-layout>
    </v-container>
  </v-layout>
</template>

<script>
import ProjectCard from '@/components/ProjectCard.vue';

export default {
  name: 'Projects',
  components: {
    'project-card': ProjectCard,
  },
  props: {
    items: {
      type: Array,
      required: true,
    },
  },
  methods: {
    selectStatus(status) {
      this.selected = status;
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
          label: 'Active',
          value: 1,
        },
        {
          label: 'Archived',
          value: 2,
        },
      ],
      selected: 0,
    };
  },
  computed: {
    filterProjects() {
      return this.selected ? this.items.filter(item => item.status === this.selected) : this.items;
    },
  },
};
</script>

<style lang="scss">
.project-cards.container {
  padding: 0;
}
</style>
