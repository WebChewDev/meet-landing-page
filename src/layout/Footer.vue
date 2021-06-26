<template>
  <div class="footer">
    <div class="footer__img-container">
      <div class="footer__overlay"></div>
    </div>
    <div class="footer__content-group">
      <h2 class="footer__heading">Experience more together</h2>
      <p class="footer__body">
        Stay connected with reliable HD meetings and unlimited one-on-one and
        group video sessions.
      </p>
      <Button class="footer__btn" text="Download" subText="v1.3" isSecondary />
    </div>
    <Icon version="2" class="footer__icon" />
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

  @include mq($from: tablet, $until: desktop) {
    width: 768px;
  }
  @include mq($from: desktop) {
    justify-content: center;
    /* align-items: flex-end; */
    /* padding: 116px 165px 104px 165px; */
    height: 308px;
    width: 1440px;
  }

  &__icon {
    position: absolute;
    left: 159px;
    top: 0;
    width: 56px;
    height: 140px;

    @include mq($from: tablet, $until: desktop) {
      left: 355px;
    }
    @include mq($from: desktop) {
      left: 692px;
      top: -114px;
    }
  }

  &__img-container {
    z-index: -1;
    position: absolute;
    left: 0%;
    right: 0%;
    top: 20.74%;
    bottom: 0%;
    height: 428px;
    width: 375px;

    background: url("../assets/mobile/image-footer.jpg");
    background-size: cover;

    @include mq($from: tablet, $until: desktop) {
      background: url("../assets/tablet/image-footer.jpg");
      left: 0%;
      right: 0%;
      top: 20.74%;
      bottom: 0%;
      width: 768px;
      height: 428px;
    }
    @include mq($from: desktop) {
      background: url("../assets/desktop/image-footer.jpg");
      background-repeat: no-repeat;
      background-size: cover;
      width: 1440px;
      height: 308px;
    }
  }

  &__overlay {
    height: 100%;
    width: 100%;
    opacity: 0.9;
    background: $color-primary;
  }

  &__content-group {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    @include mq($from: desktop) {
      flex-direction: row;
      justify-content: space-between;
      align-items: center;
      height: 88px;
      min-width: 1110px;
      /* margin: 50px 0 0 0; */
    }
  }

  &__heading {
    text-align: center;
    margin: 200px 0 0 0;
    @include heading-2-mb-light;

    @include mq($from: tablet, $until: desktop) {
      @include heading-1-mb-light;
      width: 457px;
      height: 88px;
    }
    @include mq($from: desktop) {
      @include heading-1-mb-light;
      margin: 0;
      width: 457px;
      height: 88px;
      text-align: left;
    }
  }

  &__body {
    height: 78px;
    width: 321px;
    text-align: center;
    margin: 24px 0 32px 0;
    @include body-mb-light;

    @include mq($from: tablet, $until: desktop) {
      width: 573px;
      height: 52px;
    }
    @include mq($from: desktop) {
      text-align: left;
    }
  }

  &__btn {
  }
}
</style>
Î
