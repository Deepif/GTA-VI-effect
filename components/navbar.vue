<script setup lang="ts">

import V_logo from "public/svg/V_logo.vue";
import Hamburger from "~/components/menu/hamburger.vue";
</script>

<template>
  <nav class="flex content-center items-center p-15 justify-between fixed w-full z-100">
    <div class="w-[45px] h-[45px] hover:text-yellow content-center">
      <NuxtLink to="/">
        <v_logo/>
      </NuxtLink>
    </div>
    <div>
      <hamburger/>
    </div>
  </nav>
</template>

<style scoped>

</style>