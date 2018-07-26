<template>
  <v-card>
    <v-card-title primary-title v-bind:style="{ 'background-color': color}">
      <v-icon left dark class="pb-3">assignment</v-icon>
      <base-headline
        v-bind:title="card.title"
        v-bind:description="card.description"
        class="pb-4"
        v-bind:tColor="titleTextColor"
        v-bind:dColor="descriptionTextColor"
      >
      </base-headline>
    </v-card-title>
    <v-spacer></v-spacer>
    <v-card-actions>
      <v-spacer></v-spacer>
      <v-btn flat small
        v-bind:ripple="false"
        v-for="action in actions"
        v-bind:key="action.label"
        v-on:click="action.callback(card)"
      >
        {{ action.label }} <v-icon right>{{ action.icon }}</v-icon>
      </v-btn>
      <v-spacer></v-spacer>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  name: 'UXMethodCard',
  props: {
    card: {
      type: Object,
      required: true,
    },
    actions: {
      type: Array,
      required: false,
      default: () => [],
    },
    color: String,
    titleTextColor: String,
    descriptionTextColor: String,
  },
};
</script>

<style lang="scss" scoped>
.primary-title {
  height: 200px;
}
</style>
