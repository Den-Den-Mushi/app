<script setup lang="ts">
defineProps<{
  name: string;
  model: string;
}>();
</script>

<template>
  <div class="text-center">
    <Model
      class="h-[300px] mb-3"
      :model="model"
      interaction-prompt="none"
      camera-orbit="270deg 80deg 120%"
      auto-rotate
    />
    <h1 class="font-bold text-2xl">{{ name }}</h1>
  </div>
</template>
