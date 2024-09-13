<template>
  <div>
    <h1>Hello</h1>
    <div class="alerts">
      <SuperAlert type="success">allerte succès</SuperAlert>
      <SuperAlert type="danger">allerte danger</SuperAlert>
      <SuperAlert type="error">allerte error</SuperAlert>
    </div>
  </div>
</template>

<script>
import SuperAlert from '@/components/SuperAlert.vue';

export default {
  components: {
    SuperAlert
  },
};
</script>

<style scoped>
.alerts {
  display: flex;
  gap: 1rem;
}
</style>