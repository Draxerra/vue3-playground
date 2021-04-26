<template>
  <nav class="m-nav">
    <m-nav-item class="m-nav__item" to="/">Home</m-nav-item>
    <m-nav-item class="m-nav__item" to="/movies">Movies</m-nav-item>
  </nav>
</template>

<script>
import MNavItem from "~/src/components/atoms/MNavItem";

export default {
  components: {
    "m-nav-item": MNavItem,
  },
};
</script>

<style lang="scss" scoped>
.m-nav {
  height: 100%;
  &__item {
    display: inline-flex;
    place-items: center;
    padding: 0 1.25em;
    height: 100%;
  }
}
</style>
