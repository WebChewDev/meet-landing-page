<template>
  <div>
    <ul class="gallery">
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
.gallery {
  display: grid;
  grid-template-rows: 143px 143px;
  grid-template-columns: 151px 151px;
  grid-gap: 25px 24px;
  min-height: 310px;
  margin: 0 24px;
}

.gallery__cell {
  margin: 0 auto;
}

img {
  height: 143px;
  width: 151px;
  border-radius: 8px;
}
</style>
