<template>
  <div id="app">
    <Home/>
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/> -->
  </div>
</template>

<script lang="ts">
import Home from '@/views/Home.vue';

export default {
  components:{
    Home,
  }
}
</script>

<style src="./styles/main.scss" lang="scss" />
