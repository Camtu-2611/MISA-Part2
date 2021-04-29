<template>
  <div class="home">
    <Sidebar/>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import Sidebar from '@/components/layout/Siderbar.vue'; // @ is an alias to /src

export default Vue.extend({
  name: 'Home',
  components: {
    Sidebar,
  },
});
</script>
