<template>
  <div class="syrup" :style="{'--syrup-color': syrupColor}"></div>
</template>

<script setup lang="ts">
  import { currentSyrup, currentBase } from '../stores/beverage';
  import { computed } from 'vue';
  const syrupColor = computed(() =>
    (currentSyrup.value.id === "s1") 
    ? currentBase.value.color
    : currentSyrup.value.color 
  )
</script>

<style lang="scss" scoped>
.syrup {
  transform: translateY(400%);
  // background-color: #c6c6c6;
  background-color: var(--syrup-color);
  position: relative;
  width: 100%;
  height: 20%;
  animation: pour-tea 2s 1s forwards;
  z-index: 2;
}
</style>
