<template>
  <v-container fluid fill-height class="project">
    <v-layout
      v-bind:class="{'mx-5': $vuetify.breakpoint.mdAndUp, 'mx-2': $vuetify.breakpoint.mdAndDown}"
      fill-height
      justify-space-between
    >
      <v-flex
        xs12 md9 fill-height
        v-bind:class="{'pr-5': $vuetify.breakpoint.mdAndUp}"
      >
        <v-layout column fill-height>
          <v-flex
            class="white py-4 elevation-1"
            v-bind:class="{
              'px-5': $vuetify.breakpoint.mdAndUp,
              'px-3': $vuetify.breakpoint.mdAndDown
            }"
          >
          <v-layout row justify-space-between align-start>
            <base-headline
              title="Google Reactor Project"
              size="lg"
            >
            </base-headline>
            <div>
              <v-btn color="primary">
                <v-icon left dark>add</v-icon>
                Use a Template
              </v-btn>
            </div>
          </v-layout>
          <v-divider class="mb-4"></v-divider>
          <discovery-phase v-bind:items="discoveryPhaseSteps"></discovery-phase>
          <v-divider class="my-5"></v-divider>
          <insights-discovery-phase v-bind:items="insightsDiscoveryPhaseSteps"></insights-discovery-phase>
          </v-flex>
        </v-layout>
      </v-flex>
      <v-layout column class="ux-process" hidden-sm-and-down>
      </v-layout>
    </v-layout>
  </v-container>
</template>

<script>
import DiscoveryPhase from '@/components/DiscoveryPhase.vue';
import InsightsDiscoveryPhase from '@/components/InsightsDiscoveryPhase.vue';

export default {
  name: 'Project',
  components: {
    'discovery-phase': DiscoveryPhase,
    'insights-discovery-phase': InsightsDiscoveryPhase
,  },
  data() {
    return {
      discoveryPhaseSteps: [
        {
          id: 1,
          title: 'Problem Statements',
          description: 'Winning solutions help customers get a job done better and/or more cheaply',
        },
        {
          id: 2,
          title: 'Personas',
          description: 'Winning solutions help customers get a job done better and/or more cheaply',
        },
        {
          id: 3,
          title: 'Consumer Journey Maps',
          description: 'Winning solutions help customers get a job done better and/or more cheaply',
        },
        {
          id: 4,
          title: 'Empathy Maps',
          description: 'Winning solutions help customers get a job done better and/or more cheaply',
        },
      ],
      insightsDiscoveryPhaseSteps: [
        {
          id: 1,
          title: 'Problem Statements',
          description: 'Winning solutions help customers get a job done better and/or more cheaply',
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
</style>
