<template>
  <div class="container">
      <h1>About</h1>
  </div>
</template>

<script>
export default{
  layout: 'guest.layout',
  head(){
    return{
        title: 'About Page'   
    }
  },
  mounted() {
    this.$nextTick(() => {
      this.$nuxt.$loading.start()
      setTimeout(() => this.$nuxt.$loading.finish(), 500)
    })
  }
}
</script>

<style>
</style>
