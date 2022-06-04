<script setup lang="ts">
import "@google/model-viewer";

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
    />
  </ClientOnly>
</template>
