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


    <div class="fill-pink size-8 rotate-180">
      <arrow/>
    </div>

    <div class="fade_overlay">
      <img src="/img/mask.png" alt=""/>
    </div>

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
  <section class="outro">
    <p>Looking forward to seeing what Rockstar has in store for us</p>
  </section>
</template>

<style scoped>
 img {
   width: 100%;
   height: 100%;
   object-fit: cover;
 }

 h1 {
   text-transform: uppercase;
   font-size: 6rem;
   font-weight: var(--font-weight-title);
   letter-spacing: -0.1rem;
   line-height: 0.9;
 }

 p {
   text-transform: uppercase;
   font-size: var(--font-weight-regular);
   line-height: 0.9;
 }

 section {
   position: relative;
   width: 100vw;
   height: 100vh;
   background: var(--color-dark);
   text-align: center;
   overflow: hidden;
 }

 .hero_img_container, .hero_img_container img, .fade_overlay {
   position: absolute;
   top: 0;
   left: 0;
   width: 100%;
   height: 100%;
 }

 .hero_img_logo img {
   position: absolute;
   top: 5%;
   left: 50%;
   margin-left: 10%;
   transform: translate(-50%, 0);
   width: 900px;
   height: auto;
   object-fit: contain;
 }
</style>