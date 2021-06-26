<template>
  <div>
    <img
      class="icon"
      v-if="this.version === '1'"
      src="@/assets/icon.svg"
      alt="icon 1"
    />
    <img
      class="icon"
      v-if="this.version === '2'"
      src="@/assets/icon2.svg"
      alt="icon 2"
    />
  </div>
</template>

<script>
export default {
  name: "Icon",
  props: {
    version: String,
  },
};
</script>

<style lang="scss" scoped></style>
