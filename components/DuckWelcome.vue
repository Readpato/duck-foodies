<script setup lang="ts">
const title = 'Duck nuxt starter'
</script>

<template>
  <main flex="~ col justify-center items-center" w-full h-100dvh text-white bg-black>
    <img w-12 h-12 src="~/assets/img/nuxt.png" alt="Nuxt logo" data-test="welcome-logo">
    <h1 text-2xl font-light data-test="welcome-header">
      {{ title }}
    </h1>
    <DuckCounter />
  </main>
</template>
