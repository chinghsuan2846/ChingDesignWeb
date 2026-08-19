<template>
  <section class="result bg-danger background">
    <div class="fixed-bg d-flex justify-content-start align-items-center">
      <video
        ref="bgVideo"
        :src="bgVideoSrc"
        autoplay
        muted
        loop
        playsinline
        webkit-playsinline
        preload="auto"
      ></video>
    </div>
    <div class="container-xl d-flex flex-column align-items-center">
      <BaseDot text="成果後記" class="pb-4" />
      <p class="mb-0">
        {{ props.content }}
      </p>
    </div>
  </section>
</template>

<script setup>
import BaseDot from '@/components/Dot.vue'

import { ref, onMounted } from 'vue'

const props = defineProps({
  content: { type: String, required: true },
})

const bgVideo = ref(null)
const baseUrl = import.meta.env.BASE_URL
const userAgent = navigator.userAgent
const isIOS = /iPad|iPhone|iPod/.test(userAgent) ||
  (navigator.platform === 'MacIntel' && navigator.maxTouchPoints > 1)
const isSafari = /Safari/i.test(userAgent) && !/Chrome|CriOS|Android/i.test(userAgent)
const bgVideoSrc = isIOS || isSafari
  ? `${baseUrl}Globe/SectionAnimation/iOSAnimation.mov`
  : `${baseUrl}Globe/SectionAnimation/chromeAnimation.webm`

onMounted(() => {
  const video = bgVideo.value
  if (!video) return

  video.muted = true
  video.defaultMuted = true
  video.load()

  const playPromise = video.play()
  playPromise?.catch(() => {
    // Safari 仍可能依系統設定阻擋自動播放，此時保留背景色作為降級畫面。
  })
})
</script>

<style scoped>
.result {
  width: 100%;
  position: relative; /* 讓 .fixed-bg 以 section 為基準定位 */
  z-index: 10;
  padding: 100px 176px;
  overflow: hidden; /* 避免影片超出 */
}
@media (max-width: 992px) {
  .result {
    padding: 60px 24px;
  }
}
.fixed-bg {
  position: absolute;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  z-index: 0;
  pointer-events: none; /* 不影響點擊 */
  overflow: hidden;
}

.fixed-bg video {
  width: 85%;
  height: 100%;
  overflow: visible;
}
</style>
