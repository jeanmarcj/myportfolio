<template>
  <div class="footer-wrapper">
    <hr />
    <footer class="py-5">
      <ul>
        <li class="text-secondary">
          Portfolio développé en HTML, SASS et JavaScript
        </li>
        <li class="text-secondary">
          Framework
          <a
            href="https://fr.vuejs.org/index.html"
            target="_blank"
            class="text-secondary"
          >
            Vue.JS
          </a>
        </li>
        <li>
          <a
            href="https://github.com/jeanmarcj/myportfolio"
            target="_blank"
            class="text-secondary"
          >
            <b-icon-github scale="1.2"></b-icon-github>
          </a>
        </li>
      </ul>
    </footer>
  </div>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style scoped lang="scss">
.footer-wrapper {
  height: 5rem;
  margin: 0 auto;
  hr {
    margin-top: 3rem;
    background-color: var(--text-primary-color);
  }
  footer {
    ul {
      margin: 0;
      padding: 0;
    }
  }
}
li {
  list-style: none;
  font-size: 0.8rem;
  color: var(--text-primary-color);
}

@media (min-width: 768px) {
  li {
    text-align: right;
    font-size: 1rem;
  }
}
</style>
