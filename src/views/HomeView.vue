<script>
  // Import Swiper Vue.js components
  import { Swiper, SwiperSlide } from 'swiper/vue';

  // Import Swiper styles
  import 'swiper/css';

  export default {
    data() {
      return {
        images: [
          {
            img: "https://imgs.search.brave.com/BDfLYbzPjSMFGCdqQsY6Swws1mcv-0QWdHi_cawkiQ8/rs:fit:860:0:0/g:ce/aHR0cHM6Ly93d3cu/bmVwYWxtb3VudGFp/bnRyZWtrZXJzLmNv/bS93cC1jb250ZW50/L3VwbG9hZHMvMjAy/MS8wMi9wYW5jaC1w/b2toYXJpLTIuanBn",
            title: "Pachphokahri",
          },
          {
            img: "https://imgs.search.brave.com/SaEjS7Pw4UMan9wD1b0Lz2YxcEMOibxWirlGGFTgkAM/rs:fit:860:0:0/g:ce/aHR0cDovL3RyYXZl/bGxpbmduZXBhbHRp/cHMuY29tL3dwLWNv/bnRlbnQvdXBsb2Fk/cy8yMDE4LzAyL2Ft/YXlhbmdyaS03NzB4/NDMzLmpwZw",
            title: "Amayangri",
          },
          {
            img: "https://imgs.search.brave.com/DW7JH79drojawWOdDLueob_iUkzT0ZtwkBhvjoSCmgQ/rs:fit:860:0:0/g:ce/aHR0cHM6Ly9oaWtl/b250cmVrcy5jb20v/d3AtY29udGVudC91/cGxvYWRzLzIwMTgv/MDcvZ29zYWlrdW5k/YS1zY2FsZWQuanBn",
            title: "Gosikunda",
          },
        ],
      };
    },
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      const onSwiper = (swiper) => {
        console.log(swiper);
      };
      const onSlideChange = () => {
        console.log('slide change');
      };
      return {
        onSwiper,
        onSlideChange,
      };
    },
  };
</script>

<template>
  <swiper
   class=" h-[70vh]"
    :slides-per-view="1"
    @swiper="onSwiper"
    @slideChange="onSlideChange"
  >
    <swiper-slide  v-for="(image, index) in images" :key="index">
      <img :src="image.img" alt="Slide Image"  class="  object-contain w-full"/>
      <p>{{ image.title }}</p>
    </swiper-slide>
  </swiper>
</template>
