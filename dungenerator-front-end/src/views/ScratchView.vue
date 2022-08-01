<script setup>
import DungeneratorHeader from "../components/DungeneratorHeader.vue";
import DungeneratorInput from "../components/DungeneratorInput.vue";
</script>

<template>
  <main>
    <DungeneratorHeader>
      <template #header>Generate</template>
      <template #body>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Suscipit velit
        facilis fugiat perferendis repellat repellendus recusandae voluptates
        architecto hic voluptatibus, deserunt harum minima maxime fuga ut nulla
        vel. Facilis, recusandae.
      </template>
    </DungeneratorHeader>
    <DungeneratorInput />
  </main>
</template>

<style>
.item {
  margin-top: 2rem;
  display: flex;
  flex-direction: column;
}

.details {
  flex: 1;
  margin-left: 1rem;
}

h3 {
  font-size: 1.5rem;
  font-weight: 500;
  margin-bottom: 0.4rem;
  color: var(--color-heading);
}
body {
  margin-bottom: 1rem;
}

@media (min-width: 1024px) {
  .item {
    margin-top: 0;
    padding: 0.4rem 2rem 1rem calc(var(--section-gap) / 8);
  }
}
</style>
