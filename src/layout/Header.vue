<template>
  <div class="header">
    <!-- logo -->
    <a href="/" class="header__link">
      <Logo />
    </a>
    <img class="header__image" src="@/assets/tablet/image-hero.png" alt="" />
    <h1 class="header__heading">Group Chat for Everyone</h1>
    <div class="header__body">
      Meet makes it easy to connect with others face-to-face virtually and
      collaborate across any device.
    </div>
    <Button class="header__btn-primary" text="Download" subText=" v1.3" />
    <Button
      class="header__btn-secondary"
      text="What is it?"
      width="139px"
      background="#855FB1"
    />

    <Icon class="header__icon" />
  </div>
</template>

<script>
import Icon from "../components/Icon.vue";
import Button from "../components/Button.vue";
import Logo from "../components/Logo.vue";

export default {
  name: "Header",
  components: {
    Icon,
    Button,
    Logo,
  },
};
</script>

<style lang="scss" scoped>
@import "@/scss/main.scss";

.header {
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  /* overflow: hidden; */
  height: 953px;
  width: 375px;

  &__link {
    width: 119px;
    height: 28px;
    margin: 48px 0 54px 0;
  }

  &__image {
    width: 414px;
    height: 153px;
    margin: 0 0 48px 0;
  }

  &__heading {
    @include heading-1-mb;
    text-align: center;
    width: 327px;
    height: 88px;
    margin: 0 0 24px 0;
  }

  &__body {
    @include body-mb;
    text-align: center;
    width: 327px;
    height: 78px;
    margin: 0 0 32px 0;
  }

  &__btn-primary {
    margin: 0 0 16px 0;
  }

  &__icon {
    position: absolute;
    width: 56px;
    height: 140px;
    left: 160px;
    top: 749px;
  }
}
</style>
