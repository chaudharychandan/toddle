<template>
  <v-app id="app">
    <app-header />
    <v-divider class="p-header-height"></v-divider>
    <router-view/>
  </v-app>
</template>

<script>
import Header from '@/components/Header.vue';

export default {
  name: 'ToddleApp',
  components: {
    'app-header': Header,
  },
};
</script>

<style lang="styl">
@import './assets/styles/stylus/main.styl';
@import '~vuetify/src/stylus/main.styl';
</style>

<style lang="scss">
@import './assets/styles/app.scss';
</style>

<style lang="scss" scoped>
@import './assets/styles/_vars.scss';
#app {
  height: 100%;
  background-color: $app-background-color;
  .p-header-height {
    padding-top: 64px;
  }
}
</style>
