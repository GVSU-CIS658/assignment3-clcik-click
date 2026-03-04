<template>
  <div class="baseBeverage" :style="{'--base-color': baseColor}"></div>
</template>

<script setup lang="ts">
  import { currentBase } from '../stores/beverage';
  import { computed } from 'vue';
  const baseColor = computed(() => currentBase.value.color) 
</script>

<style scoped>
.baseBeverage {
  position: relative;
  width: 100%;
  height: 100%;
  bottom: 0;
  animation: pour-tea 2s;
  z-index: 300;
  background-color: var(--base-color);
  /* // border-radius: 0.05em 0.05em 2.2em 2.2em; */
}
</style>
