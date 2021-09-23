<template>
  <div id="app">
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/portfolio">Portfolio</router-link>
    </div> -->
    <router-view />
  </div>
</template>

<script>
export default {
  data() {
    return {
      active: true,
    };
  },
  components: {},
};
</script>

<style lang="scss"></style>
