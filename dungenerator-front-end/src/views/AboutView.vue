<script setup>
import AboutComponent from "../components/AboutComponent.vue";
</script>

<template>
  <div class="about">
    <AboutComponent />
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
