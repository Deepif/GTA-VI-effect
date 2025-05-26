<script setup lang="ts">

</script>

<template>
  <div class="hamburger">
      <span/>
      <span/>
  </div>
</template>

<style scoped>
  .hamburger {
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
    width: 75px;
    height: 66px;
    padding: 1.25em;
    cursor: pointer;
    position: relative;
  }

  .hamburger span {
    width: 100%;
    height: 6px;
    background: var(--color-main);
  }

  .hamburger:hover span {
    background: var(--color-yellow);
  }
</style>