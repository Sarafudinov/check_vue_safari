<script setup>
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
 <HelloWorld />
</template>

<style scoped>
</style>

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
