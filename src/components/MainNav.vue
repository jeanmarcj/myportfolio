<template>
  <div class="container">
    <b-navbar toggleable="lg" type="dark" variant="black">
      <b-navbar-brand tag="h1" class="mb-0">Jean-Marc Juif</b-navbar-brand>
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <!-- <b-nav-item href="#">Administration</b-nav-item> -->
        </b-navbar-nav>

        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <!-- <b-icon-moon
            variant="danger"
            font-scale="2"
            class="border border-danger rounded p-2"
          ></b-icon-moon> -->
          <!-- <b-icon-brightness-high
            variant="light"
            font-scale="2.5"
            class="border border-secondary rounded bg-secondary p-2"
          ></b-icon-brightness-high> -->
          <ThemeButton />
          <!-- Drop Down -->
          <b-nav-item-dropdown text="Lang" right>
            <b-dropdown-item href="#">EN</b-dropdown-item>
            <b-dropdown-item href="#">FR</b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
import ThemeButton from "@/components/ThemeButton.vue";

export default {
  name: "MainNavbar",
  components: { ThemeButton },
};
</script>

<style>
#dropDownFR,
#dropDownEN {
  color: var(--text-primary-color);
}
</style>
