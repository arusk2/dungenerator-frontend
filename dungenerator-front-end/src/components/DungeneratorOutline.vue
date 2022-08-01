<script setup></script>

<template>
  <div class="title">
    <div class="details">
      <div class="left-edge"></div>
      <!-- Header Slot -->
      <h2>
        <slot name="header"> </slot>
      </h2>
      <!-- Slot for the body of the item -->
      <slot> </slot>
    </div>
  </div>
</template>

<style scope>
.title {
  margin-top: 2rem;
  display: flex;
}

.details {
  flex: 1;
  margin-left: 1rem;
}

h2 {
  font-size: 1.5rem;
  font-weight: 500;
  margin-bottom: 0.4rem;
  color: var(--color-heading);
}
.left-edge {
  display: flex;
  place-items: center;
  place-content: center;
  width: 32px;
  height: 32px;

  color: var(--color-text);
}
@media (min-width: 1024px) {
  .title {
    margin-top: 0;
    padding: 0.4rem 0 1rem calc(var(--section-gap) / 2);
  }

  .left-edge {
    top: calc(50% - 25px);
    left: -26px;
    position: absolute;
    /* border: 1px solid var(--color-border);
    background: var(--color-background);
    border-radius: 8px; */
    width: 50px;
    height: 50px;
  }

  .title:before {
    content: " ";
    border-left: 1px solid var(--color-border);
    position: absolute;
    left: 0;
    bottom: calc(50% + 25px);
    height: calc(50% - 25px);
  }

  .title:after {
    content: " ";
    border-left: 1px solid var(--color-border);
    position: absolute;
    left: 0;
    top: calc(50% + 25px);
    height: calc(50% - 25px);
  }

  .tile:first-of-type:before {
    display: none;
  }

  .title:last-of-type:after {
    display: none;
  }
}
</style>
