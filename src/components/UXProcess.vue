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
    <v-divider></v-divider>
  </v-flex>
</template>

<script>

export default {
  name: 'UXProcess',
  components: {
  },
  props: {
  },
};
</script>

<style scoped lang="scss">
.ux-steps-container {
  overflow: scroll;
  height: calc(100vh - 333px);
}
</style>
