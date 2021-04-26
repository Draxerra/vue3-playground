<template>
  <header class="m-header">
    <div class="m-header__logo">FilmDB</div>
    <m-nav class="m-header__nav" />
  </header>
</template>

<script>
import MNav from "~/src/components/molecules/MNav";

export default {
  components: {
    "m-nav": MNav,
  },
};
</script>

<style lang="scss" scoped>
@use "src/styles/breakpoints" as breakpoints;

.m-header {
  height: 100px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: var(--black-color);
  padding: var(--spacing);

  &__logo {
    font-size: var(--l-text);
    font-weight: bold;
    color: var(--white-color);
  }

  &__nav {
    display: none;
    @include breakpoints.sm {
      display: block;
    }
  }
}
</style>
