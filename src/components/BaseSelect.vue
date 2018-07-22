<template>
  <v-select
    :items="list"
    dense
    outline
    hide-details
    single-line
    height="40"
    max-width="150"
    self
    v-model="selected"
    item-text="label"
    item-value="value"
    v-on:change="$emit('change', selected)"
    class="t-dropdown"
  ></v-select>
</template>

<script>
export default {
  props: {
    list: Array,
    default: Number || String,
  },
  data() {
    return {
      selected: this.default,
    };
  },
};
</script>

<style lang="scss">
.t-dropdown.v-select {
  width: 150px;
  .v-input__append-inner {
    margin-top: 8px !important;
  }
  &.v-text-field--outline {
    .v-input__slot {
      min-height: 40px;
      border: 2px solid #F5F5F5;
    }
  }
}
</style>
