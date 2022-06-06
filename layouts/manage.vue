<script setup lang="ts">
const denDenMushis = ref([
  {
    id: "mXJ7xH",
    name: "Rihan's Den Den Mushi",
    model: "/model/scene.gltf",
  },
  {
    id: "sYPZHM",
    name: "Kesh's Den Den Mushi",
    model: "/model/scene.gltf",
  },
]);

function scroll(event) {
  console.log("event");
}
</script>

<template>
  <div class="flex overflow-x-auto snap-x snap-mandatory" @scroll="scroll">
    <div class="min-w-full h-screen snap-start relative" v-for="denDenMushi in denDenMushis" :key="denDenMushi.id">
      <slot v-if="$route.params.manage === denDenMushi.id" />
      <HeaderBasic :name="denDenMushi.name" :model="denDenMushi.model" v-else />
    </div>
  </div>
</template>
