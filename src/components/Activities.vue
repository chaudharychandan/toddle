<template>
  <div class="mx-1 px-3">
    <activity-log
      v-for="item in sortActivities"
      v-bind:key="item.id"
      v-bind:activity="item"
    >
    </activity-log>
  </div>
</template>

<script>
import ActivityLog from '@/components/ActivityLog.vue';

export default {
  name: 'Activities',
  components: {
    'activity-log': ActivityLog,
  },
  props: {
    items: {
      type: Array,
      required: true,
    },
  },
  computed: {
    sortActivities() {
      return Array.from(this.items).sort((item1, item2) => item1.timestamp - item2.timestamp);
    },
  },
};
</script>

<style scoped lang="scss">
</style>
