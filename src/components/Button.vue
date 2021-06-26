<template>
  <div class="button-wrapper">
    <button :style="styles" class="btn" :class="this.onHover()">
      {{ text }}
      <span :class="this.setSubTextColor()">{{ subText }}</span>
    </button>
  </div>
</template>

<script>
export default {
  name: "Button",
  props: {
    text: String,
    subText: String,
    isSecondary: Boolean,
    width: String,
  },
  computed: {
    styles() {
      return {
        width: this.width,
      };
    },
  },

  methods: {
    onHover() {
      return this.isSecondary === true ? "btn__secondary" : "btn__primary";
    },
    setSubTextColor() {
      return this.isSecondary === true
        ? "btn__subtext-secondary"
        : "btn__subtext-primary";
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
  color: $color-white;
  @include btn-text;

  &__primary {
    background: $color-primary;
  }

  &__primary:hover {
    background: $color-hvr-primary;
  }

  &__secondary {
    background: $color-secondary;
  }
  &__secondary:hover {
    background: $color-hvr-secondary;
  }

  /* Button text */

  &__subtext-primary {
    color: $color-hl-primary;
  }
  &__subtext-secondary {
    color: $color-hl-secondary;
  }
}
</style>
