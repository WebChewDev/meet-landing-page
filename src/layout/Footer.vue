<template>
  <div class="footer">
    <div class="footer__img-container">
      <!-- <img
        class="footer__bgImage"
        src=""
        alt=""
      /> -->
      <div class="footer__overlay"></div>
    </div>

    <Icon class="footer__icon" />
    <h2 class="footer__heading">Experience more together</h2>
    <p class="footer__body">
      Stay connected with reliable HD meetings and unlimited one-on-one and
      group video sessions.
    </p>
    <Button
      text="Download"
      subText="v1.3"
      :subTextColorAlt="true"
      background="#855FB1"
      class="footer__btn"
    />
  </div>
</template>

<script>
import Button from "../components/Button.vue";
import Icon from "../components/Icon.vue";

export default {
  name: "Footer",
  components: {
    Button,
    Icon,
  },
};
</script>

<style lang="scss" scoped>
@import "@/scss/main.scss";

.footer {
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  height: 540px;
  width: 375px;

  &__img-container {
    z-index: -1;
    position: absolute;
    left: 0%;
    right: 0%;
    top: 20.74%;
    bottom: 0%;
    height: 428px;
    width: 375px;
    background: url("../assets/mobile/image-footer.jpg") red;
    background-size: cover;
  }

  &__overlay {
    height: 100%;
    width: 100%;
    opacity: 0.9;
    background: $color-primary;
  }

  &__bgImage {
    z-index: -1;
    position: absolute;
    left: 0%;
    right: 0%;
    top: 20.74%;
    bottom: 0%;
    height: 428px;
    width: 375px;
    background: purple;
  }

  &__heading {
    text-align: center;
    margin: 200px 0 0 0;
    @include heading-2-mb-light;
  }

  &__body {
    height: 78px;
    width: 321px;
    text-align: center;
    margin: 24px 0 32px 0;
    @include body-mb-light;
  }

  &__btn {
  }

  &__icon {
    position: absolute;
    left: 159px;
    top: 0;
    width: 56px;
    height: 140px;
  }
}
</style>
Î
