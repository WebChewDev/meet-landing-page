<template>
  <div class="feature">
    <Gallery class="feature__gallery" />
    <p class="feature__overline">Built for modern use</p>
    <h2 class="feature__heading">Smarter meetings, all in one place</h2>
    <p class="feature__body">
      Send messages, share files, show your screen, and record your meetings —
      all in one workspace. Control who can join with invite-only team access,
      data encryption, and data export.
    </p>
  </div>
</template>

<script>
import Gallery from "../components/Gallery.vue";

export default {
  name: "Feature",
  components: {
    Gallery,
  },
};
</script>

<style lang="scss" scoped>
@import "@/scss/main.scss";

.feature {
  position: relative;
  height: 722px;
  width: 375px;

  @include mq($from: tablet, $until: desktop) {
    height: 524px;
    width: 768px;
  }
  @include mq($from: desktop) {
    display: flex;
    flex-direction: column;
    align-items: center;

    height: 746px;
    width: 1440px;
  }

  &__gallery {
    margin: 0 0 64px 0;
  }

  &__overline {
    @include overline;
    height: 26px;
    text-align: center;
    margin: 0 auto 24px;

    @include mq($from: desktop) {
      margin: 0 auto 16px;
    }
  }

  &__heading {
    @include heading-2-mb;
    text-align: center;
    width: 320px;
    height: 72px;
    margin: 0 auto 24px;

    @include mq($from: tablet, $until: desktop) {
      @include heading-1-mb;
      height: 88px;
      width: 445px;
    }

    @include mq($from: desktop) {
      @include heading-2-dk;
      height: 88px;
      width: 445px;
      margin: 0 auto 32px;
    }

    @include mq($from: desktop) {
      @include heading-2-dk;
      height: 88px;
      width: 445px;
    }
  }

  &__body {
    height: 130px;
    width: 327px;
    margin: 0 auto;
    text-align: center;
    @include body-mb;

    @include mq($from: tablet, $until: desktop) {
      height: 78px;
      width: 573px;
    }
    @include mq($from: desktop) {
      height: 78px;
      width: 540px;
    }
  }
}
</style>
