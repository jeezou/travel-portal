<template>
  <Main />
</template>

<script>
import Main from "./views/Main.vue";

export default {
  name: "App",
  components: {
    Main,
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Aleo:ital,wght@0,400;0,700;1,700&family=Magra:wght@400;700&family=Red+Hat+Text:wght@400;500&display=swap");
@import url("static/reset.css");
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  overflow-x: hidden;
}
</style>
