<template>
  <router-link class="m-nav-item" :to="to"><slot /></router-link>
</template>

<script>
import { useRouter } from "vue-router";

export default {
  props: {
    to: {
      type: String,
      required: true,
    },
  },
  setup({ to }) {
    const router = useRouter();

    const goTo = () => {
      router.push(to);
    };

    return { goTo };
  },
};
</script>

<style lang="scss" scoped>
.m-nav-item {
  font-size: var(--m-text);
  color: var(--white-color);
  text-decoration: none;

  &.router-link-active {
    color: var(--primary-color);
    font-weight: bold;
  }
  &:hover {
    color: var(--primary-color);
  }
}
</style>
