<template>
  <div>
    <Header/>
    <article class="mx-auto w-11/12 lg:w-9/12 max-w-3xl">
      <slot/>
    </article>
  </div>
</template>

<script setup>
const route = useRoute();

const findEl = async (hash, x) => {
  return document.querySelector(hash) ||
      new Promise((resolve, reject) => {
        if (x > 50) {
          return resolve()
        }
        setTimeout(() => { resolve(findEl(hash, ++x || 1)) }, 100)
      })
}

if(route.hash) {
  const el = await findEl(route.hash);

  if ('scrollBehavior' in document.documentElement.style) {
    window.scrollTo({ top: el.offsetTop })
  } else {
    window.scrollTo(0, el.offsetTop)
  }
}
</script>