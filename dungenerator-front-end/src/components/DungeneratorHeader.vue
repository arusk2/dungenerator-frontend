<template>
  <div class="item">
    <div class="details">
      <h3>
        <slot name="header"></slot>
      </h3>
      <slot name="body"></slot>
    </div>
  </div>
</template>

<style scoped>
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
