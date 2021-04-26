<template>
  <movie-template>
    <router-view></router-view>
  </movie-template>
</template>

<script>
import MovieTemplate from "~/src/components/templates/Movie";

export default {
  components: {
    "movie-template": MovieTemplate,
  },
  setup() {},
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css?family=Roboto");
:root {
  --xxs-text: 1.2em;
  --xs-text: 1.4em;
  --s-text: 1.6em;
  --m-text: 2em;
  --l-text: 2.8em;
  --xl-text: 3.6em;
  --xxl-text: 4.4em;

  --primary-color: hsl(174, 57%, 72%);
  --black-color: hsl(0, 0%, 20%);
  --white-color: hsl(0, 0%, 95%);

  --spacing: 0 5rem;
  --mobile-spacing: 0 2rem;
}

body {
  margin: 0;
  font-family: "Roboto", sans-serif;
}

html {
  font-size: 10px;
}

h1,
h2,
h3,
h4,
h5,
h6 {
  margin: 0;
  font-weight: normal;
}

h1 {
  font-size: var(--xxl-text);
}

h2 {
  font-size: var(--xl-text);
}

h3 {
  font-size: var(--l-text);
}

h4 {
  font-size: var(--m-text);
}

h5 {
  font-size: var(--s-text);
}

h6 {
  font-size: var(--xs-text);
}
</style>
