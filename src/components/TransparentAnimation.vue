<template>
  <div ref="container" class="transparent-animation" aria-hidden="true"></div>
</template>

<script setup>
import lottie from 'lottie-web'
import { onBeforeUnmount, onMounted, ref } from 'vue'

const props = defineProps({
  animationPath: { type: String, required: true },
  preserveAspectRatio: { type: String, default: 'xMidYMid meet' },
})

const container = ref(null)
let animation

onMounted(() => {
  if (!container.value) return

  animation = lottie.loadAnimation({
    container: container.value,
    renderer: 'svg',
    loop: true,
    autoplay: true,
    path: `${import.meta.env.BASE_URL}${props.animationPath}`,
    rendererSettings: {
      // 保持原始比例並完整呈現，避免窄 viewport 裁掉左右動畫內容。
      preserveAspectRatio: props.preserveAspectRatio,
    },
  })
})

onBeforeUnmount(() => {
  animation?.destroy()
})
</script>

<style scoped>
.transparent-animation {
  width: 100%;
  height: 100%;
  overflow: hidden;
}

.transparent-animation :deep(svg) {
  display: block;
  width: 100%;
  height: 100%;
}
</style>
