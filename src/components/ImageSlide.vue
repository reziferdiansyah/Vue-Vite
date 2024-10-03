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
      :items-to-show="2"
      :wrap-around="true"
      v-model="currentSlide"
      ref="carousel"
    >
      <Slide
        v-for="slideThumbnails in fetchStaticImg"
        :key="slideThumbnails.id"
        style="margin: 5px !important"
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
        path: "/src/assets/images/example-img.webp",
        alt: "Images 1",
      },
      {
        id: 2,
        type: "mobile",
        path: "/src/assets/images/example-img.webp",
        alt: "Images 2",
      },
      {
        id: 3,
        type: "mobile",
        path: "/src/assets/images/example-img.webp",
        alt: "Images 3",
      },
      {
        id: 4,
        type: "mobile",
        path: "/src/assets/images/example-img.webp",
        alt: "Images 3",
      },
      {
        id: 5,
        type: "mobile",
        path: "/src/assets/images/example-img.webp",
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
