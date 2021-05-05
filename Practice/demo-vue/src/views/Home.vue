<template>
  <div class="main">
    <Sidebar />
    <div class="t-container">
      <Header />
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import Sidebar from "@/components/layout/Siderbar.vue"; // @ is an alias to /src
import Header from "@/components/layout/Header.vue";
export default Vue.extend({
  name: "Home",
  components: {
    Sidebar,
    Header,
  },
});
</script>

<style lang="scss" scoped>

.main {
  display: flex;
  width: 100%;
  height: 100vh;
  box-sizing: border-box;
}
.t-container {
  width: calc(100% - 150px);
  background-color: #e5e6eb;
}
</style>
