<!-- This example requires Tailwind CSS v2.0+ -->
<template>
  <NuxtLink :to="article._path">
    <div class="bg-white overflow-hidden shadow rounded-lg">
      <div class="px-4 py-5 sm:p-6">
        <h2 class="text-xl font-bold text-gray-900 sm:text-2xl">{{ article.title }}</h2>
        <p class="text-sm font-medium text-gray-600">{{ article.description }}</p>
      </div>
    </div>
  </NuxtLink>
</template>

<script setup>
const props = defineProps(['article'])
</script>