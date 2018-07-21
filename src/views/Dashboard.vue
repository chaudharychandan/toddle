<template>
  <v-layout v-bind:class="{'px-5 py-5 mx-5': $vuetify.breakpoint.mdAndUp, 'px-3 py-3': $vuetify.breakpoint.mdAndDown}">
    <div>Dashboard Page</div>
  </v-layout>
</template>

<script>
export default {
  name: 'Dashboard',
  components: {
  },
};
</script>

<style scoped lang="scss">
</style>
