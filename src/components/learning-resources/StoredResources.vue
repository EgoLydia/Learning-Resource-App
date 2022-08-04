<template>
  <ul>
    <learning-resource
      v-for="data in resources"
      :key="data.id"
      :title="data.title"
      :description="data.description"
      :link="data.link"
      >{{ data }}</learning-resource
    >
  </ul>
</template>

<script>
import LearningResource from './LearningResource.vue';

export default {
  components: {
    LearningResource,
  },
  inject: ['resources'],
};
</script>

<style scoped>
ul {
  list-style: none;
  margin: 0;
  padding: 0;
  margin: auto;
  max-width: 40rem;
}
</style>
