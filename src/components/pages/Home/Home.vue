<template>
  <main class="home">
    <section class="hero-section">
      <h2 class="hero-section__header">Find your favourite movies.</h2>
      <h3 class="hero-section__subheader">
        Grab some popcorn and start searching.
      </h3>
    </section>
    <img class="clapper-board" :src="clapperBoard" />
  </main>
</template>

<script>
import clapperBoard from "url:~/src/assets/clapper-board.svg";
export default {
  setup() {
    return {
      clapperBoard,
    };
  },
};
</script>

<style lang="scss" scoped>
@use "src/styles/breakpoints" as breakpoints;

.home {
  width: 100%;
  display: flex;
  flex-direction: column;
  place-items: center;
  place-content: center;
  gap: 4em;
  margin: var(--mobile-spacing);
  font-size: 0.8rem;
  @include breakpoints.md {
    flex-direction: row;
    place-content: space-around;
    margin: var(--spacing);
  }
  @include breakpoints.lg {
    font-size: 0.9rem;
  }
  @include breakpoints.xl {
    font-size: 1rem;
  }
}

.clapper-board {
  max-height: 30em;
  transform: rotate(-10deg);
  @include breakpoints.lg {
    max-height: 35em;
  }
  @include breakpoints.xl {
    max-height: 45em;
  }
}

.hero-section {
  text-align: center;
  display: flex;
  flex-direction: column;
  gap: 1em;

  @include breakpoints.md {
    text-align: left;
  }
  &__header {
    font-weight: bold;
    line-height: 1.2em;
  }
  &__subheader {
    line-height: 1.4em;
  }
}

/* .home {
  width: 100%;
  display: grid;
  grid-template-columns: 1fr 1fr;
  align-items: center;
  justify-items: center;
  gap: 5rem;
  margin: var(--spacing);
}
.clapper-board {
  max-height: 500px;
  transform: rotate(-10deg);
}
.hero-section {
  &__header {
    font-size: var(--xl-text);
    font-weight: bold;
    line-height: 1em;
    margin: 0;
    margin-bottom: 0.5em;
  }
  &__subheader {
    font-size: var(--m-text);
    font-weight: normal;
    line-height: 1.2em;
    margin-bottom: 1em;
  }
} */
</style>
