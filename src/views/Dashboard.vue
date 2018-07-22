<template>
  <v-container fluid fill-height class="dashboard">
    <v-layout
      v-bind:class="{'mx-5': $vuetify.breakpoint.mdAndUp}"
      fill-height
    >
      <v-flex  xs12 md8 fill-height>
        <v-layout column fill-height>
          <base-headline
            title="Welcome Juan Ho!"
            description="Lorem ipsum dolor sit amet, consectetur adipiscing"
            size="lg"
          >
          </base-headline>
          <v-flex class="white pa-5 elevation-1">
            <projects v-bind:items="projects"></projects>
            <v-divider class="my-5"></v-divider>
            <ux-methods v-bind:items="uxMethods"></ux-methods>
          </v-flex>
        </v-layout>
      </v-flex>
      <v-flex md4 fill-height class="pl-4" hidden-sm-and-down>
        <v-layout column fill-height>
          <base-headline
            title="Activity Map"
            description="Lorem ipsum dolor sit amet, consectetur adipiscing"
            size="lg"
          >
          </base-headline>
          <activity-map v-bind:activities="activities"></activity-map>
        </v-layout>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
import ActivityMap from '@/components/ActivityMap.vue';
import Projects from '@/components/Projects.vue';
import UXMethods from '@/components/UXMethods.vue';

export default {
  name: 'Dashboard',
  components: {
    'activity-map': ActivityMap,
    projects: Projects,
    'ux-methods': UXMethods,
  },
  data() {
    return {
      activities: [
        { title: 'A' }, { title: 'B' },
      ],
      projects: [
        {
          id: 1,
          title: 'Research',
          description: 'pdf',
          status: 1,
        },
        {
          id: 2,
          title: 'Research',
          description: 'pdf',
          status: 2,
        },
        {
          id: 3,
          title: 'Research',
          description: 'pdf',
          status: 1,
        },
        {
          id: 4,
          title: 'Research',
          description: 'pdf',
          status: 1,
        },
        {
          id: 11,
          title: 'Research',
          description: 'pdf',
          status: 2,
        },
        {
          id: 22,
          title: 'Research',
          description: 'pdf',
          status: 1,
        },
        {
          id: 33,
          title: 'Research',
          description: 'pdf',
          status: 1,
        },
        {
          id: 44,
          title: 'Research',
          description: 'pdf',
          status: 1,
        },
      ],
      uxMethods: [
        {
          id: 1,
          title: 'Jobs To Be Done',
          description: 'Winning solutions help customers get a job done better and/or more cheaply',
          type: 1,
        },
        {
          id: 2,
          title: 'Design Sprints',
          description: 'Winning solutions help customers get a job done better and/or more cheaply',
          type: 2,
        },
        {
          id: 3,
          title: 'Qualitative',
          description: 'Winning solutions help customers get a job done better and/or more cheaply',
          type: 2,
        },
        {
          id: 4,
          title: 'Quantitative',
          description: 'Winning solutions help customers get a job done better and/or more cheaply',
          type: 2,
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
</style>
