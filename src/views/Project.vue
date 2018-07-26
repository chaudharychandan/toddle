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
            class="white pb-4 elevation-1"
          >
            <v-layout
              row justify-space-between align-center
              v-bind:class="{
                'px-5 py-2': $vuetify.breakpoint.mdAndUp,
                'px-3 py-3': $vuetify.breakpoint.mdAndDown
              }"
            >
              <base-headline
                title="Google Reactor Project"
                size="md"
              >
              </base-headline>
              <div>
                <v-btn color="primary hidden-sm-and-down">
                  <v-icon left dark>add</v-icon>
                  Use a Template
                </v-btn>
              </div>
            </v-layout>
            <v-divider class="mb-4"></v-divider>
            <div v-bind:class="{
              'px-5': $vuetify.breakpoint.mdAndUp,
              'px-3': $vuetify.breakpoint.mdAndDown
            }">
              <discovery-phase v-bind:items="discoveryPhaseSteps"></discovery-phase>
              <v-divider class="my-5"></v-divider>
              <insights-discovery-phase v-bind:items="insightsDiscoveryPhaseSteps"></insights-discovery-phase>
            </div>
          </v-flex>
        </v-layout>
      </v-flex>
      <v-layout column class="ux-process" hidden-sm-and-down>
        <ux-process v-bind:steps="uxProcessSteps"></ux-process>
      </v-layout>
    </v-layout>
  </v-container>
</template>

<script>
import DiscoveryPhase from '@/components/DiscoveryPhase.vue';
import InsightsDiscoveryPhase from '@/components/InsightsDiscoveryPhase.vue';
import UXProcess from '@/components/UXProcess';

export default {
  name: 'Project',
  components: {
    'discovery-phase': DiscoveryPhase,
    'insights-discovery-phase': InsightsDiscoveryPhase,
    'ux-process': UXProcess,
  },
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
      uxProcessSteps: [
        {
          id: 1,
          title: 'Discovery Phase',
          description: 'Problem Statements, Personas, Consumer Journey Maps, Empathy Maps',
          insights: false,
          covered: true,
        },
        {
          id: 2,
          title: 'Insights: Discovery Phase',
          description: 'Problem Statements, Personas, Consumer Journey Maps, Empathy Maps',
          insights: true,
          covered: true,
        },
        {
          id: 3,
          title: 'Interpretation Phase',
          description: 'Problem Statements, Personas, Consumer Journey Maps, Empathy Maps',
          insights: false,
          covered: false,
        },
        {
          id: 4,
          title: 'Insights: Interpretation Phase',
          description: 'Problem Statements, Personas, Consumer Journey Maps, Empathy Maps',
          insights: true,
          covered: false,
        },
        {
          id: 5,
          title: 'Ideation/Strategy Phase',
          description: 'Problem Statements, Personas, Consumer Journey Maps, Empathy Maps',
          insights: false,
          covered: false,
        },
        {
          id: 6,
          title: 'Insights: Ideation/Strategy Phase',
          description: 'Problem Statements, Personas, Consumer Journey Maps, Empathy Maps',
          insights: true,
          covered: false,
        },
        {
          id: 7,
          title: 'Experimentation Phase',
          description: 'Problem Statements, Personas, Consumer Journey Maps, Empathy Maps',
          insights: false,
          covered: false,
        },
        {
          id: 8,
          title: 'Insights: Experimentation Phase',
          description: 'Problem Statements, Personas, Consumer Journey Maps, Empathy Maps',
          insights: true,
          covered: false,
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
</style>
