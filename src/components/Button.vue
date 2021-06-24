<template>
  <div class="btn-group">
    <button
      @mouseover="onHover"
      :subTextColorAlt="false"
      :style="styles"
      :class="hover"
      class="btn"
    >
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
    type: String,

    width: { type: [String], default: "193px" },
    color: { type: [String], default: "#FFFFFF" },
    background: { type: [String], default: "#4D96A9" },
  },
  data() {
    return {
      hover: "active",
    };
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
    onHover() {
      this.styles.background = "red";
      console.log(this.styles);
    },
  },
};
</script>

<style lang="scss" scoped>
@import "@/scss/main.scss";

.btn {
  height: 58px;
  width: 193px;
  border: none;
  border-radius: 29px;
  @include btn-text;
}



.btn-primary {
  
}

.hover {
  background: green;
}


</style>
