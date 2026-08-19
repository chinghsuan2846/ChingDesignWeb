<template>
  <section class="parallax-section bg-danger">
    <div
      ref="parallaxBackground"
      class="parallax-background rellax"
      :data-rellax-speed="props.speed"
      :data-rellax-xs-speed="props.mobileSpeed"
      :data-rellax-mobile-speed="props.mobileSpeed"
      :style="{ backgroundImage: `url('${props.image}')` }"
    ></div>
  </section>
</template>

<style scoped>
.parallax-section {
  height: 60vh;
  position: relative;
  z-index: 5;
}
.parallax-background {
  position: absolute;
  left: 0;
  width: 100%;
  height: 150%;
  top: -25%;
  background-size: cover;
  background-position: center center;
  will-change: transform;
  backface-visibility: hidden;
}

@media (max-width: 767.98px) {
  .parallax-section {
    height: clamp(260px, 42vh, 340px);
  }

  .parallax-background {
    height: 120%;
    top: -10%;
    background-size: 150% auto;
    background-repeat: no-repeat;
  }
}
</style>

<script setup>
import { onBeforeUnmount, onMounted, nextTick, ref } from 'vue'
import Rellax from 'rellax'

const props = defineProps({
  image: {
    type: String,
    required: true,
  },
  speed: {
    type: Number,
    default: -5,
  },
  mobileSpeed: {
    type: Number,
    default: -2,
  },
})

const parallaxBackground = ref(null)
let rellaxInstance

const initializeParallax = () => {
  if (rellaxInstance || !parallaxBackground.value) return
  rellaxInstance = new Rellax(parallaxBackground.value, { center: true })
}

onMounted(() => {
  nextTick(() => {
    const img = new Image()
    img.onload = initializeParallax
    img.onerror = initializeParallax
    img.src = props.image
    if (img.complete) initializeParallax()
  })
})

onBeforeUnmount(() => {
  rellaxInstance?.destroy()
  rellaxInstance = null
})
</script>
