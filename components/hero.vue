<script setup lang="ts">

import Arrow from "assets/arrow.vue";
import rect_svg from "~/assets/rect_svg.vue";
import Ps5_logo from "assets/ps5_logo.vue";
import Xbox_logo from "assets/xbox_logo.vue";
</script>

<template>
  <section class="hero">
    <div class="hero_img_container">
      <img src="/img/1.jpg" alt="artwork of Lucia and Jason"/>
    </div>
    <div class="hero_img_logo">
      <img src="/img/logo.png" alt="logo of Grand Theft Auto VI">
    </div>
    <img src="/img/mask.png" alt=""/>

    <div class="fill-pink size-8 rotate-180">
      <arrow/>
    </div>

    <div class="fade_overlay"></div>

    <div class="overlay">
      <rect_svg/>
    </div>

    <div class="logo_container"></div>

    <div class="content_overlay">
      <div class="logo_overlay">
        <img src="/img/vi_logo.webp" alt=""/>
      </div>
      <h1>Available May 26, 2026</h1>
      <div class="output_supports fill-main">
        <ps5_logo/>
        <xbox_logo/>
      </div>
    </div>
  </section>
  <section class="outro"></section>
</template>

<style scoped>

</style>