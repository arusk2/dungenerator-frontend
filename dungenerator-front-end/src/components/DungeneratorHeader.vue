<template>
  <div class="item">
    <div class="details">
      <h3>
        <slot name="header"></slot>
      </h3>
      <slot name="body"></slot>
      <div class="note">
        <slot name="note"></slot>
      </div>
    </div>
  </div>
</template>
