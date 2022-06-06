<script lang="ts" setup>
useHead({
  htmlAttrs: {
    lang: "en",
  },
  bodyAttrs: {
    class: "bg-gray-100",
  },
});
</script>

<template>
  <NuxtLayout>
    <Navigation />
    <NuxtPage />
  </NuxtLayout>
</template>
