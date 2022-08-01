<script setup>
import WelcomeItem from "../components/WelcomeItem.vue";
import ToolingIcon from "../components/icons/IconTooling.vue";
</script>

<template>
  <WelcomeItem>
    <template #icon>
      <ToolingIcon />
    </template>
    <template #heading>Scratch Paper</template>
    Lorem ipsum dolor sit, amet consectetur adipisicing elit. Consequatur et
    corporis amet hic, ducimus voluptatem id, pariatur ex soluta a deserunt
    porro libero enim, cupiditate laudantium harum natus atque quasi.
  </WelcomeItem>
</template>
