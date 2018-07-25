<template>
  <v-layout row>
    <v-flex md2 class="activity-timeline">
      <div class="activity-marker light-blue lighten-4">
        <span></span>
      </div>
    </v-flex>
    <v-flex md10 py-3>
      <v-layout column>
        <div class="grey--text pb-2">{{ getTime }}</div>
        <base-headline
          v-bind:title="activity.title"
          v-bind:description="activity.description"
          size="xs"
        >
        </base-headline>
        <v-flex py-3>
          <v-layout row wrap>
            <v-chip
              v-for="item in activity.types"
              v-bind:key="item"
              label
              color="grey lighten-3"
              small
            >
              {{ item }}
            </v-chip>
          </v-layout>
        </v-flex>
      </v-layout>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  name: 'Activity',
  props: {
    activity: {
      type: Object,
      required: true,
    },
  },
  computed: {
    getTime() {
      return new Date(this.activity.timestamp).toDateString();
    },
  },
};
</script>

<style scoped lang="scss">
.activity-timeline {
  position: relative;
  border-left: 4px solid #EEEEEE;
  margin-left: 6px;
  .activity-marker {
    height: 20px;
    width: 20px;
    border-radius: 50%;
    position: absolute;
    top: 20px;
    left: -12px;
    span {
      display: block;
      height: 10px;
      width: 10px;
      border-radius: 50%;
      margin: 5px;
      background-color: #03A9F4;
    }
  }
}
</style>
