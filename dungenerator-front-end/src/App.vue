<script setup>
import { RouterLink, RouterView } from "vue-router";
import TitleLine from "./components/TitleLine.vue";
</script>

<template>
  <header>
    <div class="dragon">
      <!-- Art by Ooyamaneko courtesy of ascriiart.eu -->
      <pre>
                 /           /
                /' .,,,,  ./
               /';'     ,/
              / /   ,,//,`'`
             ( ,, '_,  ,,,' ``
             |    /@  ,,, ;" `
            /    .   ,''/' `,``
           /   .     ./, `,, ` ;
        ,./  .   ,-,',` ,,/''\,'
       |   /; ./,,'`,,'' |   |
       |     /   ','    /    |
        \___/'   '     |     |
          `,,'  |      /     `\
               /      |        ~\
              '       (
             :
            ; .         \--
          :   \         ;
   </pre
      >
    </div>

    <div class="wrapper">
      <TitleLine msg="Dungeon Room Generator" />

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
.dragon {
  font-family: monospace;
  white-space: pre;
  display: block;
  margin: 7vh auto 1.5rem auto;
  line-height: 1;
}
header {
  line-height: 1.5;
  max-height: 200vh;
}

nav {
  width: 100%;
  font-size: 16px;
  text-align: center;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    flex-direction: column;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
    margin-top: -1rem;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1.5rem;
    padding: 1rem 0;
  }
}
</style>
