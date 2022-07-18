<template>
  <main class="mx-auto w-9/12 mb-20">
    <h2 class="text-2xl font-bold leading-7 text-gray-900 sm:text-3xl mb-2">Dumps</h2>
    <ContentList path="/dumps" v-slot="{ list }">
      <div class="grid grid-cols-1 sm:grid-cols-2 xl:grid-cols-3 gap-3">
        <card v-for="article in list" :key="article._path" :article="article"/>
      </div>
    </ContentList>
  </main>
</template>