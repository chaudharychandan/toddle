<template>
  <v-app id="app">
    <app-header />
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
@import './assets/style/stylus/main.styl';
@import '~vuetify/src/stylus/main.styl';
</style>

<style lang="scss">
@import './assets/style/variables.scss';
@import './assets/style/app.scss';

html, body {
  min-height: 100%;
  box-sizing: border-box;
  a {
    text-decoration: none;
  }
}
#app {
  height: 100%;
  background-color: $app-background-color;
}
</style>

