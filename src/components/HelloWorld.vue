<template>
  <swiper 
          :initial-slide="1"
          :slides-per-view="1.15"
          :space-between="10"
          :centeredSlides="true"
          :loop="false"
          :slide-to-clicked-slide="true"
          :touch-ratio="1.5"
          :pagination="true"
          :modules="modules" 
          class="mySwiper">
    <swiper-slide>Slide 1</swiper-slide>
    <swiper-slide>Slide 2</swiper-slide><swiper-slide>Slide 3</swiper-slide>
    <swiper-slide>Slide 4</swiper-slide><swiper-slide>Slide 5</swiper-slide>
    <swiper-slide>Slide 6</swiper-slide><swiper-slide>Slide 7</swiper-slide>
    <swiper-slide>Slide 8</swiper-slide><swiper-slide>Slide 9</swiper-slide>
  </swiper>
</template>
<script>
  // Import Swiper Vue.js components
  import { Swiper, SwiperSlide } from 'swiper/vue';

  // Import Swiper styles
  import 'swiper/css';

  import 'swiper/css/pagination';

  import './style.css';

  // import required modules
  import { Pagination } from 'swiper/modules';

  export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      return {
        modules: [Pagination],
      };
    },
  };
</script>

<style>
  .swiper {
    width: 100%;
    height: 100%;
  }

  .swiper-slide {
    text-align: center;
    font-size: 18px;
    background: #fff;

    display: flex;
    justify-content: center;
    align-items: center;
  }

  .swiper-slide img {
    display: block;
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  .swiper::after {
  content: '';
  position: absolute;
  bottom: env(safe-area-inset-bottom, 0px);;
  left: 0;
  right: 0;
  height: 100px;
  background: linear-gradient(to top, rgba(26, 26, 26, 1), rgba(0, 0, 0, 0));
  pointer-events: none;
  z-index: 1;
  backdrop-filter: blur(0.5px);
}
</style>
