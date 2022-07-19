<template>
  <div class="mb-5">
    <h4 v-if="title">{{ title }}</h4>
    <carousel :wrapAround="true">
      <slide v-for="imageUrl in images" :key="imageUrl">
        <img :src="imageUrl">
        {{ slide }}
      </slide>

      <template v-if="images.length > 1" #addons>
        <navigation/>
        <pagination/>
      </template>
    </carousel>
  </div>
</template>

<script setup>
import 'vue3-carousel/dist/carousel.css';
import {Carousel, Slide, Pagination, Navigation} from 'vue3-carousel';

const props = defineProps(['images', 'title'])
</script>

<style>
h4 {
  @apply mt-4 !important
}

.carousel__pagination-button {
  @apply bg-blue-200
}

.carousel__pagination-button--active {
  @apply bg-blue-500
}

.carousel__prev, .carousel__next {
  @apply bg-blue-600
}

.carousel__pagination, .carousel__pagination > * {
  @apply m-0 p-0
}

img {
  @apply m-0 !important
}
</style>