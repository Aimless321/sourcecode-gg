<template>
  <div class="grid" :class="{'gap-12': cols > 1, 'grid-cols-2': cols == 2, 'grid-cols-3': cols == 3, 'grid-cols-4': cols == 4}">
    <slot/>
  </div>
</template>

<script setup>
const props = defineProps(['cols'])
</script>