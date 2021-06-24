<template>
  <div>
    <img v-if="this.version === '1'" src="@/assets/icon.svg" alt="" />
    <img v-if="this.version === '2'" src="@/assets/icon2.svg" alt="" />
  </div>
</template>

<script>
// console.log(this.icon1)

export default {
  name: "Icon",
  props: {
    version: String,
  },
  data() {
    return {
      icon1: "../assets/icon.svg",
      icon2: "@/assets/icon2.svg",
    };
  },
  methods: {
    renderIcons() {
      return this.version === "1" ? "@/assets/icon.svg" : "@/assets/icon2.svg";
    },
  },
};
</script>

<style></style>
