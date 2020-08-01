<template>
  <div class="">
      <h1>BLog Item</h1>
      <p>{{ params.post }}</p>
  </div>
</template>

<script>
export default {
  layout: 'guest.layout',
  validate({ params }) {
    console.log('validate: ', params);
    return true;
  },
  data() {
    return {
      params: this.$route.params,
    }
  }
}
</script>

<style>

</style>