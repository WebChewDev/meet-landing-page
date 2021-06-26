<template>
  <div>
    <ul :style="styles" class="gallery">
      <li class="gallery__cell" v-for="(image, index) in images" :key="index">
        <img :src="image.image" :alt="image.alt" />
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Gallery",

  data() {
    return {
      images: [
        {
          image: require("@/assets/desktop/image-woman-in-videocall.jpg"),
          alt: "woman in videocall",
        },
        {
          image: require("@/assets/desktop/image-man-texting.jpg"),
          alt: "man texting",
        },
        {
          image: require("@/assets/desktop/image-men-in-meeting.jpg"),
          alt: "Men in meeting",
        },
        {
          image: require("@/assets/desktop/image-women-videochatting.jpg"),
          alt: "Women on video call",
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
@import "@/scss/main.scss";

.gallery {
  display: grid;
  grid-template-rows: 143px 143px;
  grid-template-columns: 151px 151px;
  grid-gap: 25px 24px;
  min-height: 310px;
  min-width: 327px;
  margin: 0 24px;

  @include mq($from: tablet, $until: desktop) {
    min-height: 156px;
    min-width: 689px;

    grid-template-rows: none;
    grid-template-columns: repeat(4, 151px);
  }
  @include mq($from: desktop) {
    min-width: 1110px;
    min-height: 242px;

    grid-template-rows: none;
    grid-template-columns: repeat(4, 242px);
    grid-gap: 30px
  }
}

.gallery__cell {
  height: 100%;
  widows: 100%;
  margin: 0 auto;
}

img {
  height: 143px;
  width: 151px;
  border-radius: 8px;

  @include mq($from: desktop) {
    width: 255px;
    height: 242px;
  }
}
</style>
