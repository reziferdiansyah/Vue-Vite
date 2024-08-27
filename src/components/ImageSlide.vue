<template>
  <div>
    <!-- LIST MASTER -->
    <Carousel
      :autoplay="2000"
      id="gallery"
      :items-to-show="1"
      :wrap-around="true"
      v-model="currentSlide"
    >
      <Slide v-for="slide in fetchStaticImg" :key="slide.id">
        <div class="carousel__item">
          <img :alt="slide.alt" :src="slide.path" />
        </div>
      </Slide>
    </Carousel>

    <!-- PREVIEW -->
    <Carousel
      id="thumbnails"
      :items-to-show="3"
      :wrap-around="true"
      v-model="currentSlide"
      ref="carousel"
    >
      <Slide
        v-for="slideThumbnails in fetchStaticImg"
        :key="slideThumbnails.id"
        style="margin: 10px !important"
      >
        <div class="carousel__item" @click="slideTo(slideThumbnails.id - 1)">
          <img :alt="slideThumbnails.alt" :src="slideThumbnails.path" />
        </div>
      </Slide>
    </Carousel>
  </div>
</template>

<script>
import { defineComponent } from "vue";
import { Carousel, Slide } from "vue3-carousel";
import "vue3-carousel/dist/carousel.css";

export default defineComponent({
  name: "ImageSlide",
  components: {
    Carousel,
    Slide,
    Navigation,
  },

  data() {
    const staticImages = [
      {
        id: 1,
        type: "mobile",
        path: "https://cktch.sgp1.cdn.digitaloceanspaces.com/staging/banner/mobile/77d8ba99973a43ee370272bb94e05369.webp",
        alt: "Images 1",
      },
      {
        id: 2,
        type: "mobile",
        path: "https://cktch.sgp1.cdn.digitaloceanspaces.com/staging/banner/mobile/c9928a05bee4490a6ff84ef6903db1b2.webp",
        alt: "Images 2",
      },
      {
        id: 3,
        type: "mobile",
        path: "https://cktch.sgp1.cdn.digitaloceanspaces.com/staging/banner/mobile/4120ba70fe5358fe249b8061c668cf7d.webp",
        alt: "Images 3",
      },
      {
        id: 4,
        type: "mobile",
        path: "https://cktch.sgp1.cdn.digitaloceanspaces.com/staging/banner/mobile/c4b5df8307a036787c23adcc7debfd3d.webp",
        alt: "Images 3",
      },
    ];
    return {
      currentSlide: 0,
      fetchStaticImg: staticImages,
    };
  },

  methods: {
    slideTo(val) {
      this.currentSlide = val;
    },
  },
});
</script>
