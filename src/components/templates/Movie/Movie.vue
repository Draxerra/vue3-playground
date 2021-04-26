<template>
  <div class="movie-template">
    <m-header class="movie-template__header" />
    <div class="movie-template__content"><slot /></div>
    <m-snackbar class="movie-template__snackbar" />
  </div>
</template>

<script>
import MHeader from "~/src/components/organisms/MHeader";
import MSnackbar from "~/src/components/organisms/MSnackbar";
export default {
  components: {
    "m-header": MHeader,
    "m-snackbar": MSnackbar,
  },
  setup() {},
};
</script>

<style lang="scss" scoped>
@use "src/styles/breakpoints" as breakpoints;

.movie-template {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  &__content {
    display: flex;
    flex: 1;
  }
}
</style>
