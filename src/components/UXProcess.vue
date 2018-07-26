<template>
  <v-flex class="white elevation-1">
    <v-layout row justify-space-between align-center py-2 px-3>
      <base-headline
        title="UX Process"
        size="md"
      >
      </base-headline>
      <div>
        <v-btn flat color="grey">
          Customize Process
        </v-btn>
      </div>
    </v-layout>
    <v-layout column>
      <div v-for="step in steps" v-bind:key="step.id">
        <v-divider></v-divider>
        <ux-process-step v-bind:step="step">
        </ux-process-step>
      </div>
    </v-layout>
  </v-flex>
</template>

<script>
import UXProcessStep from '@/components/UXProcessStep.vue';

export default {
  name: 'UXProcess',
  components: {
    'ux-process-step': UXProcessStep,
  },
  props: {
    steps: Array,
    required: true,
  },
};
</script>

<style scoped lang="scss">
.ux-steps-container {
  overflow: scroll;
  height: calc(100vh - 333px);
}
</style>
