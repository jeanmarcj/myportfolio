<template>
  <div class="formation-wrapper">
    <b-row class="my-3">
      <b-col cols="12" md="2" class="d-flex align-items-center">
        <div class="formation-raw-line"></div>
        <div class="formation-raw-circle ml-2"></div>
      </b-col>
      <b-col
        cols="12"
        md="3"
        class="mt-2 d-flex align-items-center formation-text"
      >
        <div class="formation-raw-text">
          <div class="formation-raw-text-header">
            <strong>{{ header }}</strong>
          </div>
          <div class="ormation-raw-text-company">{{ company }}</div>
          <div class="formation-raw-text-date">{{ date }}</div>
        </div>
      </b-col>
      <b-col cols="12" md="7" class="mt-3 d-flex align-items-center">
        <div class="formation-raw-description">
          <p>{{ description }}</p>
        </div>
      </b-col>
    </b-row>
    <!-- Row end -->
  </div>
</template>

<script>
export default {
  name: "Formations",
  props: {
    header: String,
    company: String,
    date: String,
    description: String,
  },
};
</script>

<style lang="scss">
.formation-raw-line {
  height: 0.125rem;
  width: 5rem;
  background-color: #dc3545;
}
.formation-raw-circle {
  height: 0.5rem;
  width: 0.5rem;
  border-radius: 9999px;
  background-color: #dc3545;
  display: none;
}
.formation-raw-text {
  color: var(--text-primary-color);
}
.formation-raw-text-date {
  font-size: 0.875rem;
  line-height: 1.25rem;
}
.formation-raw-description {
  font-weight: 450;
  color: var(--text-primary-color);
}

@media (min-width: 768px) {
  .formation-raw-circle {
    display: block;
  }
  .formation-raw-text {
    // border: 1px solid green;
    margin-left: -2.5rem;
  }
}
</style>
