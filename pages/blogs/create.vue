<template>
  <div class="card">
      <h2>Create post</h2>
      <form @submit.prevent="submit">
          <input type="text" class="form-control" v-model="title" placeholder="Enter Title"><br>
          <textarea class="form-control" v-model="body"></textarea>
          <button class="btn btn-block btn-primary">Submit</button>
      </form>
  </div>
</template>

<script>
export default {
    layout: 'guest.layout',
    data() {
        return{
            title: '',
            body: '',
        }
    },
    head() {
        return{
            title: 'Create Post'
        }
    },
    methods: {
        submit() {
            this.$nuxt.$loading.start();
            this.$axios.$post('https://jsonplaceholder.typicode.com/posts', {
                userId: 200,
                id: 12,
                title: this.title,
                description: this.body
            }).then(response => {
                console.log('response',response)
            }).finally(
                this.$nuxt.$loading.finish()
            ); 
        }
    }
}
</script>

<style>

</style>