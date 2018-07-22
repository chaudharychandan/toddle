<template>
  <v-card>
    <v-card-title primary-title>
      <base-headline
        v-bind:title="method.title"
        v-bind:description="method.description"
        class="pb-5"
      >
      </base-headline>
    </v-card-title>
    <v-spacer></v-spacer>
    <v-card-actions>
      <v-spacer></v-spacer>
      <v-btn flat small>
        Use this <v-icon right>arrow_right_alt</v-icon>
      </v-btn>
      <v-spacer></v-spacer>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  name: 'UXMethodCard',
  props: {
    method: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style lang="scss" scoped>
.primary-title {
  height: 200px;
}
</style>
