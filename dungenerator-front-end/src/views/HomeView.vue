<script setup>
import DungeneratorHeader from "../components/DungeneratorHeader.vue";
import DungeneratorInput from "../components/DungeneratorInput.vue";
</script>

<template>
  <main>
    <DungeneratorHeader>
      <template #header>Generate Rooms</template>
      <template #body>
        Enter a few words to give the model something to start with. Each
        sentence generated will start with this seed phrase. <br />
        Then, indicate the number of unique sentences you'd like the model to
        generate and click generate to get the proccess started! <br /><br />
      </template>
      <template #note>
        * Note: currently, generation can take 5-30 seconds. I am working to
        speed up inference times.
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
.note {
  font-size: 0.8rem;
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
    padding: 0.4rem 2rem 1rem calc(var(--section-gap) / 10);
  }
}
</style>
