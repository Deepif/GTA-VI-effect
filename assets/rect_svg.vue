<script setup>
defineProps({
  path: String
})
</script>

<template>
  <svg width="100%" height="100%">
    <defs>
      <mask id="revealLogo">
        <rect width="100%" height="100%" fill="white"/>
        <path :d="path" fill="black" />
      </mask>
    </defs>
    <rect
        width="100%"
        height="100%"
        fill="#111"
        mask="url(#revealLogo)"
    />
  </svg>
</template>