<template>
  <v-container fluid fill-height class="dashboard">
    <v-layout
      v-bind:class="{'my-5 mx-5': $vuetify.breakpoint.mdAndUp}"
      fill-height
    >
      <v-flex  xs12 md8 fill-height>
        <v-layout column fill-height>
          <dashboard-subheader
            title="Welcome Juan Ho!"
            description="Lorem ipsum dolor sit amet, consectetur adipiscing"
          >
          </dashboard-subheader>
          <v-flex class="white pa-5 elevation-1">
          </v-flex>
        </v-layout>
      </v-flex>
      <v-flex md4 fill-height class="pl-4" hidden-sm-and-down>
        <v-layout column fill-height>
          <dashboard-subheader
            title="Activity Map"
            description="Lorem ipsum dolor sit amet, consectetur adipiscing"
          >
          </dashboard-subheader>
          <activity-map v-bind:activities="activities"></activity-map>
        </v-layout>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
import DashboardSubheader from '@/components/DashboardSubheader.vue';
import ActivityMap from '@/components/ActivityMap.vue';

export default {
  name: 'Dashboard',
  components: {
    'activity-map': ActivityMap,
    'dashboard-subheader': DashboardSubheader,
  },
  data() {
    return {
      activities: [
        { title: 'A' }, { title: 'B' },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
</style>
