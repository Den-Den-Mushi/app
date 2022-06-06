<script setup lang="ts">
if (process.client) import("@google/model-viewer");

defineProps<{
  model: string;
  poster?: string;
  alt?: string;
}>();
</script>

<template>
  <ClientOnly>
    <model-viewer
      class="w-full"
      :alt="alt"
      :src="model"
      :poster="poster"
      shadow-intensity="1"
      camera-controls
      disable-zoom
      @contextmenu.prevent
      v-bind="$attrs"
    />
  </ClientOnly>
</template>

<style scoped>
model-viewer {
  --poster-color: transparent;
}
</style>
