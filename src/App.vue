<template>
  <div id="app">
    <h1 class="heading">HELLO</h1>
    <h2 class="subheading">Lorem ipsum dolor sit amet.</h2>
    <p class="overline">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Sunt, deserunt?
    </p>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {},
};
</script>

<style lang="scss">
@import "@/scss/main.scss";

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.heading {
  @include heading-1;
}

.subheading {
  @include heading-2;
}

.overline {
  @include overline;
}
</style>
