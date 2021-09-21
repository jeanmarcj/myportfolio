<template>
  <div id="app">
    <MainNav></MainNav>
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/portfolio">Portfolio</router-link>
    </div> -->
    <router-view />
  </div>
</template>

<script>
import MainNav from "./components/MainNav.vue";
export default {
  data() {
    return {
      active: true,
    };
  },
  components: {
    MainNav,
  },
};
</script>

<style lang="scss"></style>
