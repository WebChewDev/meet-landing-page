<template>
  <div class="header">
    <!-- logo -->
    <a href="/" class="header__link">
      <Logo />
    </a>
    <div class="header__content-wrapper">
      <div class="header__image-left" alt=""></div>
      <div class="header__image-right" alt=""></div>
      <div class="header__image" alt=""></div>

      <div class="header__content-group">
        <h1 class="header__heading">Group Chat for Everyone</h1>
        <div class="header__body">
          Meet makes it easy to connect with others face-to-face virtually and
          collaborate across any device.
        </div>
        <div class="header__btn-group">
          <Button class="header__btn-primary" text="Download" subText=" v1.3" />
          <Button
            class="header__btn-secondary"
            text="What is it?"
            width="139px"
            isSecondary
          />
        </div>
      </div>
    </div>

    <Icon version="1" class="header__icon" />
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

  @include mq($from: tablet, $until: desktop) {
    height: 1064px;
    width: 768px;
  }

  @include mq($from: desktop) {
    width: 1440px;
    height: 841px;
  }

  &__link {
    width: 119px;
    height: 28px;
    margin: 80px 0 61px 0;
  }

  &__content-wrapper {
    @include mq($from: desktop) {
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      width: 1440px;
    }
  }

  &__content-group {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    @include mq($from: desktop) {
      height: 358px;
      width: 540px;
      order: 2;
    }
  }

  &__image {
    background-image: url("../assets/tablet/image-hero.png");
    background-size: cover;
    width: 414px;
    height: 153px;
    margin: 0 0 48px 0;

    @include mq($from: tablet, $until: desktop) {
      background-image: url("../assets/tablet/hero-tablet.jpg");
      background-size: inherit;
      background-repeat: no-repeat;
      background-position: center;
      margin: 0 0 72px 0;
      height: 303px;
      width: 820px;
    }

    @include mq($from: desktop) {
      display: none;
    }
  }

  &__image-left {
    @include mq($from: desktop) {
      background-image: url("../assets/desktop/image-hero-left.png");
      background-size: cover;
      background-position: right;
      align-self: flex-start;

      height: 303px;
      width: 362px;
      order: 1;
    }
  }
  &__image-right {
    @include mq($from: desktop) {
      background-image: url("../assets/desktop/image-hero-right.png");
      background-size: cover;
      align-self: flex-end;
      height: 303px;
      width: 362px;
      order: 3;
    }
  }

  &__heading {
    @include heading-1-mb;
    text-align: center;
    width: 327px;
    height: 88px;
    margin: 0 0 24px 0;

    @include mq($from: tablet, $until: desktop) {
      @include heading-1-tab;
    }

    @include mq($from: desktop) {
      @include heading-1-dk;
      margin: 47px 0 34px 0;
      width: 445px;
      height: 128px;
    }
  }

  &__body {
    @include body-mb;
    text-align: center;
    width: 327px;
    height: 78px;
    margin: 0 0 32px 0;

    @include mq($from: tablet, $until: desktop) {
      height: 52px;
      width: 457px;
    }
    @include mq($from: desktop) {
      height: 52px;
      width: 540px;
    }
  }

  &__btn-group {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    @include mq($from: tablet) {
      flex-direction: row;
      justify-content: space-between;
      height: 58px;
      width: 348px;
    }
  }

  &__btn-primary {
    margin: 0 0 16px 0;

    @include mq($from: tablet) {
      margin: 0 0 0 0;
    }
  }

  &__icon {
    position: absolute;
    width: 56px;
    height: 140px;
    left: 160px;
    top: 749px;

    @include mq($from: tablet, $until: desktop) {
      left: 356px;
      top: 857px;
    }
    @include mq($from: desktop) {
      left: 692px;
      top: 637px;
    }
  }
}
</style>
