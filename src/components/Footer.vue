<template>
  <div class="footer-wrapper">
    <hr />
    <footer class="py-5 text-right">
      <ul class="mt-3">
        <li class="mr-3">Portfolio développé en HTML, SASS et JavaScript</li>
        <li class="mr-3">
          Framework <a href="https://fr.vuejs.org/index.html">Vue.JS</a>
        </li>
        <li class="mr-3">
          <a href="https://github.com/jeanmarcj/myportfolio">
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
  }
}
li {
  list-style: none;
  font-size: 0.8rem;
}
</style>
