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
@import url("https://fonts.googleapis.com/css2?family=Red+Hat+Display:wght@500;900&display=swap");

html {
  font-family: "Red Hat Display", sans-serif;
  display: flex;
  justify-content: center;
}

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  margin: 0 auto;
  min-height: 2215px;

  @include mq($from: tablet, $until: desktop) {
    min-width: 768px;
    min-height: 2128px;
  }

  @include mq($from: desktop) {
    width: 1440px;
    min-height: 1895px;
  }
}
</style>
