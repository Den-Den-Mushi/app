<script lang="ts" setup>
useHead({
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
