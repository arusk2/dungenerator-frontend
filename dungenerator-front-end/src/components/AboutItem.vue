<template>
  <div class="about-item">
    <div class="profile-pic">
      <slot name="icon"></slot>
    </div>
    <div class="details">
      <h3>
        <slot name="heading"></slot>
      </h3>
      <slot></slot>
    </div>
  </div>
</template>

<style scoped>
.about-item {
  margin-top: 2rem;
  display: flex;
}

.details {
  flex: 1;
  margin-left: 1rem;
  /* left: 40px; */
}

.profile-pic {
  width: 20%;
  margin-left: 0.8rem;
}

h3 {
  font-size: 1.2rem;
  font-weight: 500;
  margin-bottom: 0.4rem;
  color: var(--color-heading);
}
/* 
@media (min-width: 1024px) {
  .about-item {
    margin-top: 2rem;
    padding: 0.4rem 0 1rem calc(var(--section-gap) / 2);
  }

  i {
    top: calc(50% - 25px);
    left: 40px;
    position: absolute;
    width: 50px;
    height: 50px;
  }
} */
</style>
