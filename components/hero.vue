<script setup lang="js">

import Arrow from "assets/arrow.vue";
import rect_svg from "~/assets/rect_svg.vue";
import Ps5_logo from "assets/ps5_logo.vue";
import Xbox_logo from "assets/xbox_logo.vue";
import {onMounted, ref} from 'vue'
import gsap from "gsap";
import {logoData} from "assets/gta_6_logo_white.vue";


const heroContainer = ref(null)
const heroImgLogo = ref(null)
const scrollCont = ref(null)
const fadeOverlay = ref(null)
const logoOverlay = ref(null)
const outro = ref(null)
const logoContainer = ref(null)
const logoMask = ref(null)
const initialOverlayScale = 350

onMounted(() => {

})


</script>

<template>
  <section class="hero">
    <div class="hero_img_container" ref="heroContainer">
      <img src="/img/1.jpg" alt="artwork of Lucia and Jason"/>
    </div>
    <div class="hero_img_logo" ref="heroImgLogo">
      <img src="/img/logo.png" alt="logo of Grand Theft Auto VI">
    </div>

    <div class="scroll_container" ref="scrollCont">
      <div class="fill-pink size-8 rotate-180">
        <arrow/>
      </div>
    </div>

    <div class="fade_overlay" ref="fadeOverlay">
      <img src="/img/mask.png" alt=""/>
    </div>

    <div class="overlay" ref="logoOverlay">
      <rect_svg :path="logoData"/>
    </div>

    <div class="logo_container" ref="logoContainer"></div>

    <div class="content_overlay" ref="outro">
      <div class="logo_overlay">
        <img src="/img/vi_logo.webp" alt=""/>
      </div>
      <h1>Available May 26, 2026</h1>
    </div>
    <div class="output_supports fill-main">
      <ps5_logo/>
      <xbox_logo/>
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

 .scroll_container {
   position: absolute;
   bottom: 10%;
   left: 50%;
   transform: translateX(-50%);
   will-change: opacity;
 }

 .fade_overlay {
   background-color: var(--color-main);
   will-change: opacity;
 }

 .overlay {
   position: absolute;
   top: 0;
   left: 0;
   transform-origin: center 15%;
   width: 100%;
   height: 250%;
   z-index: 1;
 }

 .logo_container {
   position: fixed;
   top: 25%;
   left: 50%;
   transform: translate(-50%, -50%);
   width: 200px;
   height: 150px;
   z-index: 2;
 }

.content_overlay {
  position: absolute;
  bottom: 25%;
  left: 50%;
  transform: translateX(-50%);
  z-index: 2;
}

.logo_overlay {
  position: absolute;
  bottom: 25%;
}

.content_overlay h1 {
  background-clip: text;
  -webkit-text-fill-color: transparent;
  -webkit-background-clip: text;
  color: transparent;
  transform-origin: center;
}

.logo_overlay img {
  display: none;
}

.outro {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>