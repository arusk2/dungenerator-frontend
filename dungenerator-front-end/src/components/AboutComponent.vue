<script setup>
import AboutItem from "./AboutItem.vue";
</script>

<template>
  <!-- Insert header describing project and link to dataset here.
    Need link to gpt2 and link to artist -->
  <div class="item">
    <div class="details">
      <div class="header">
        <h3>About This Project</h3>
      </div>
      This is a free, passion project that uses OpenAI's
      <a href="https://openai.com/blog/better-language-models/">GPT-2</a>
      language model to generate novel descriptions of rooms you could find
      while dungeon delving with your party of adventurers in The Worlds Most
      Popular Roleplaying Game.
    </div>
    <div class="details">
      The GPT-2 model was trained on the
      <a href="https://github.com/arusk2/dungeons-and-datasets"
        >Dungeons and Datasets
      </a>
      dataset that collects spoken and written descriptions of dungeon rooms
      from a variety of sources.
    </div>
    <AboutItem>
      <template #icon>
        <img
          class="profile-icon"
          src="../assets/AndrewRuskampWhiteHeadshot.png"
          alt="Andrew Ruskamp-White"
        />
      </template>
      <template #heading> Andrew Ruskamp-White</template>
      Lorem ipsum dolor sit, amet consectetur adipisicing elit. Assumenda
      quibusdam quia tempore expedita quisquam perspiciatis vero odio excepturi
      magni, libero vel praesentium quod et. Iste culpa modi et est itaque?
    </AboutItem>
  </div>
</template>

<style scoped>
h3 {
  font-size: 1.5rem;
  font-weight: 500;
  margin-bottom: 0.4rem;
  color: var(--color-heading);
}

img {
  width: 100%;
  height: 100%;
  border-radius: 50%;
}
</style>
