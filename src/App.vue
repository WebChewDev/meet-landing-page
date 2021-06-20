<template>
  <div id="app">
    <Header />
    <Feature />
    <Footer />
  </div>
</template>

<script>
import Header from "./layout/Header.vue";
import Feature from "./layout/Feature.vue";
import Footer from "./layout/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Feature,
    Footer,
  },
};
</script>

<style lang="scss">
@import "@/scss/main.scss";

html {
  display: flex;
  justify-content: center;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  margin: 0 auto;
  min-height: 2215px;
  width: 375px;

  /* border: 1px solid black; */
}
</style>
