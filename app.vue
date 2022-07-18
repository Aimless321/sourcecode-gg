<template>
  <div>
    <NuxtLayout>
      <NuxtPage/>
    </NuxtLayout>
  </div>
</template>

<script setup>
import 'assets/css/main.css'

useHead({
  titleTemplate: (titleChunk) => {
    return titleChunk ? `${titleChunk} - Sourcecode\'s brain dump` : 'Sourcecode\'s brain dump';
  },
  viewport: 'width=device-width, initial-scale=1, maximum-scale=1',
  charset: 'utf-8',
})
</script>