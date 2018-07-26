<template>
  <v-layout row justify-space-between v-bind:class="{ 'grey lighten-5' : step.covered }">
    <div class="ux-process-icon pa-4">
      <v-icon
        v-bind:color="step.covered ? 'light-blue darken-4' : 'teal accent-4'"
        medium
      >
        {{getIcon}}
      </v-icon>
    </div>
    <v-flex md11 py-3 pr-3>
      <v-layout column>
        <base-headline
          v-bind:title="step.title"
          v-bind:description="step.description"
          size="xs"
          v-bind:t-color="step.covered ? '#01579B' : ''"
        >
        </base-headline>
      </v-layout>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  name: 'UXProcessStep',
  props: {
    step: Object
  },
  computed: {
    getIcon() {
      return this.step.insights ? 'timeline' : 'explore';
    },
  },
};
</script>

<style scoped lang="scss">

</style>
