<template>
  <div class="btn-group">
    <button :subTextColorAlt="false" :style="styles" class="btn">
      {{ text }}
      <span :style="this.handleSubTextAlt()">{{ subText }}</span>
    </button>
  </div>
</template>

<script>
export default {
  name: "Button",
  props: {
    text: String,
    subText: String,
    subTextColorAlt: Boolean,
    isColor: String,

    width: { type: [String], default: "193px" },
    color: { type: [String], default: "#FFFFFF" },
    background: { type: [String], default: "#4D96A9" },
  },
  computed: {
    styles() {
      return {
        width: this.width,
        color: this.color,
        background: this.background,
      };
    },
  },
  methods: {
    handleSubTextAlt() {
      return {
        color: this.subTextColorAlt === true ? "#D9B8FF" : "#8FE3F9",
      };
    },
  },
};
</script>

<style lang="scss" scoped>
@import "@/scss/main.scss";

/* .btn-group{
  margin: 0;
  padding: 0;
  height: 0;
  width: 0;
} */

.btn {
  height: 58px;
  width: 193px;
  border: none;
  border-radius: 29px;
  @include btn-text;
}

.btn-primary {
  background: red;
}

.hover {
  background: green;
}
</style>
