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
      while dungeon delving with your party of adventurers in a fantasy
      role-playing game.
    </div>
    <div class="details">
      This GPT-2 model was trained on data from
      <a href="https://github.com/arusk2/dungeons-and-datasets"
        >Dungeons and Datasets,
      </a>
      a collection of spoken and written descriptions of dungeon rooms from a
      variety of sources.
    </div>
    <div class="details">
      Special thanks to
      <a href="https://github.com/sciwizard">Joel Williams</a> and
      <a href="https://github.com/zachgrow">Zach Grow</a> who both worked with
      me on creating Dungeons and Datasets.
    </div>
    <div class="details">
      <div class="note">
        ASCII art by
        <a href="https://www.asciiart.eu/mythology/dragons">Ooyamaneko</a>.
      </div>
    </div>
    <AboutItem>
      <template #icon>
        <img
          class="profile-icon"
          src="../assets/AndrewRuskampWhiteHeadshot.png"
          alt="Andrew Ruskamp-White"
        />
      </template>
      <template #heading>Andrew Ruskamp-White</template>
      <template #body>
        Your friendly neighborhood computer scientist and nerd.
      </template>
      <template #twitter-link
        ><a href="https://twitter.com/ARuskampWhite">Twitter</a></template
      >
      <template #github-link>
        <a href="https://github.com/arusk2/">Github</a></template
      >
    </AboutItem>
  </div>
</template>

<style scoped>
.note {
  font-size: 0.8rem;
}
.details {
  margin-bottom: 1rem;
}
h3 {
  font-size: 1.5rem;
  font-weight: 500;
  margin-bottom: 0.4rem;
  color: var(--color-heading);
}

img {
  /* width: 100%; */
  /* height: 100%; */
  border-radius: 50%;
  max-width: 110px;
  max-height: 120px;
}
</style>
