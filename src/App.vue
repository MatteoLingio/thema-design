<template>
  <div id="app">
    <Grid>
      <div
        v-for="i in Array.from({ length: 12 }, (x, i) => i)"
        :key="i"
        style="background-color: red;"
        class="col sm-12 md-4 lg-3 xl-1"
      ></div>
    </Grid>
  </div>
</template>

<script>
import Grid from "./components/Grid";

export default {
  name: "app",
  components: { Grid }
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;600;700&family=Poppins:wght@400;500;700&display=swap");
@import "./assets/styles/_colors.scss";
@import "./assets/styles/_typography.scss";

html {
  box-sizing: border-box;
  font-size: 16px;
}

*,
*:before,
*:after {
  box-sizing: inherit;
}

body {
  margin: 0;
  padding: 0 0 0;
  font-family: $primary-font;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#app {
  display: flex;
}
</style>
