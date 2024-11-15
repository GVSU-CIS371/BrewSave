<template>
  <div
    class="syrup"
    :style="{
      background: `repeating-linear-gradient(
        45deg,
        ${currentSyrup || 'transparent'},
        ${currentSyrup || 'transparent'} 10px,
        rgba(225, 207, 149, 1) 10px,
        rgba(225, 207, 149, 1) 20px
      )`,
    }"
  ></div>
</template>

<script setup lang="ts">
import { currentSyrup } from "../stores/beverage";
</script>
<style lang="scss" scoped>
.syrup {
  transform: translateY(400%);
  background-color: #c6c6c6;
  position: relative;
  width: 100%;
  height: 20%;
  animation: pour-tea 2s 1s forwards;
  z-index: 2;
}
</style>
