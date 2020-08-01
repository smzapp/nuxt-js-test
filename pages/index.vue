<template>
  <div class="container">
    Welcome index
  </div>
</template>

<script>
export default{
  layout: 'guest.layout',
  head() {
    return {
      title: 'Home page',
      meta: [
        {
          hid: 'description', // remove duplicate meta
          name: 'description', 
          content: 'welcome to home page',
        }
      ],
      script: [{src: '/about.js'}]
    }
  },
  mounted() {
    this.$nextTick(() => {
      this.$nuxt.$loading.start()
      setTimeout(() => this.$nuxt.$loading.finish(), 500)
    })
  },
}
</script>

<style>
</style>
