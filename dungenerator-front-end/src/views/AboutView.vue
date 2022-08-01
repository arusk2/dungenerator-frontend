<script setup>
import ClickerComponent from "@/components/ClickerComponent.vue";
</script>

<template>
  <div class="about">
    <ClickerComponent />
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
