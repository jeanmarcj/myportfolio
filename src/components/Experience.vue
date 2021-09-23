<template>
  <div class="position-relative d-flex align-items-center">
    <div class="experience-vertical-bar bg-danger"></div>
    <div class="experience-circle-round bg-danger"></div>
    <div class="experience-content">
      <p class="experience-content-header font-weight-bold">
        {{ header }}
      </p>
      <p class="experience-content-header">
        {{ company }}
      </p>
      <p class="experience-content-date">{{ period }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    header: String,
    company: String,
    period: String,
  },
};
</script>

<style scoped lang="scss">
.experience-vertical-bar {
  position: absolute;
  width: 0.125rem;
  height: 5rem;
  top: 3.5rem;
  left: 0.2rem;
  background-color: #dc3545;
}
.experience-circle-round {
  height: 0.5rem;
  width: 0.5rem;
  border-radius: 9999px;
  background-color: #dc3545;
}
.experience-content {
  margin-left: 2rem;
  .experience-content-header {
    font-size: 1rem;
    line-height: 1.5rem;
    margin: 0;
  }
  .experience-content-date {
    margin-top: 0.125rem;
    font-size: 0.875rem;
    line-height: 1.25rem;
  }
}
</style>
