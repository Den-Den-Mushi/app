<script lang="ts" setup>
useHead({
  htmlAttrs: {
    lang: "en",
  },
  bodyAttrs: {
    class: "bg-gray-100 mx-auto container",
  },
});
</script>

<template>
  <NuxtLayout>
    <Navigation />
    <NuxtPage />
  </NuxtLayout>
</template>
