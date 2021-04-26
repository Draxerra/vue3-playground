<template>
  <footer class="m-snackbar">
    <m-nav class="m-snackbar__nav" />
  </footer>
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

.m-snackbar {
  height: 7.5em;
  background-color: var(--black-color);
  padding: var(--spacing);

  @include breakpoints.sm {
    display: none;
  }

  &__nav {
    display: flex;
    place-content: center;
  }
}
</style>
