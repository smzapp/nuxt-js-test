<template>
  <div id="main-app">
    <div class="container">
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
      <router-link to="/blogs">Blogs</router-link>
      <router-link to="/blogs/post-item-here">Posts</router-link>
      <router-link to="/blogs/create">Create</router-link>
    </div>
    <div class="container">
      <transition>
      <nuxt/>
      </transition>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>

</style>