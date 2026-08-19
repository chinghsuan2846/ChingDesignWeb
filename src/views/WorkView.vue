<script setup>
import { RouterLink } from 'vue-router'
import { ref, onMounted } from 'vue'
import TransparentAnimation from '@/components/TransparentAnimation.vue'

const bgVideo = ref(null)
const baseUrl = import.meta.env.BASE_URL
const userAgent = navigator.userAgent
const useTransparentAnimation = /iPad|iPhone|iPod/.test(userAgent) ||
  (navigator.platform === 'MacIntel' && navigator.maxTouchPoints > 1) ||
  (/Safari/i.test(userAgent) && !/Chrome|CriOS|Android/i.test(userAgent))

onMounted(() => {
  const video = bgVideo.value
  if (!video) return

  video.muted = true
  video.defaultMuted = true
  const tryPlay = () => {
    if (video.paused) video.play().catch(() => {})
  }
  video.addEventListener('loadeddata', tryPlay, { once: true })
  video.load()
  tryPlay()
})
</script>

<template>
  <div class="fixed-bg d-flex justify-content-start align-items-center">
    <TransparentAnimation
      v-if="useTransparentAnimation"
      animation-path="Globe/SectionAnimation/SectionAnimation.json"
      class="transparent-animation-bg"
    />
    <video
      v-else
      ref="bgVideo"
      autoplay
      muted
      loop
      playsinline
      webkit-playsinline
      preload="auto"
    >
      <source :src="`${baseUrl}Globe/SectionAnimation/chromeAnimation.webm`" type="video/webm" />
      <source :src="`${baseUrl}Globe/SectionAnimation/iOSAnimation.mov`" type="video/quicktime" />
    </video>
  </div>
  <section class="relative background">
    <div class="container">
      <h2 class="text-dark h1 pb-8 mb-0 fw-medium pt-8">Work</h2>
      <div class="row g-16">
        <div class="col-md-6 col-12">
          <RouterLink to="/work/chargingStation" class="text-decoration-none work-link">
            <div class="work-image-wrap">
              <img
                src="/Work_Overview/ChargingStationDSSDesign.jpg"
                alt="work-img-2"
                class="img-fluid work-img"
              />
            </div>
            <div class="tag pt-8" @click.stop>
              <span class="button border border-1 border-success text-success lh-170 me-3">
                Web
              </span>
              <span class="button border border-1 border-success text-success lh-170">
                DSS Design
              </span>
            </div>
            <h3 class="text-success fs-8 lh-170 fw-medium pt-4 pb-3 m-0">智慧開電選址系統</h3>
            <p class="lh-170">
              一套企業內部的智慧選址決策系統，用於評估充電站場址的開發潛力，整合地理與商業數據，提供多維度評分分析。
            </p>
          </RouterLink>
        </div>
        <div class="col-md-6 col-12">
          <RouterLink to="/work/lineLiff" class="text-decoration-none work-link">
            <div class="work-image-wrap">
              <img src="/Work_Overview/LINELiff.jpg" alt="work-img-1" class="img-fluid work-img" />
            </div>
            <div class="tag pt-8" @click.stop>
              <span class="button border border-1 border-success text-success lh-170 me-3">
                Moible
              </span>
              <span class="button border border-1 border-success text-success lh-170">
                LINE Liff Design
              </span>
            </div>
            <h3 class="text-success fs-8 lh-170 fw-medium pt-4 pb-3 m-0">
              星舟快充 LINE Liff 設計
            </h3>
            <p class="lh-170">
              星舟快充致力於電動車充電服務，本次改版優化 LINE 操作介面，讓使用者充電更直覺順暢。
            </p>
          </RouterLink>
        </div>
        <div class="col-md-6 col-12">
          <RouterLink to="/work/eomc" class="text-decoration-none work-link">
            <div class="work-image-wrap">
              <img
                src="/EOMC/overview.jpg"
                alt="企業營運中心管理系統"
                class="img-fluid work-img"
              />
            </div>
            <div class="tag pt-8" @click.stop>
              <span class="button border border-1 border-success text-success lh-170 me-3">
                Web
              </span>
              <span class="button border border-1 border-success text-success lh-170">
                Dashboard
              </span>
            </div>
            <h3 class="text-success fs-8 lh-170 fw-medium pt-4 pb-3 m-0">企業營運中心管理系統</h3>
            <p class="lh-170">
              整合各事業單位的營運與財務資料，透過模組化資訊架構與清楚的狀態設計，協助主管快速掌握營運狀況。
            </p>
          </RouterLink>
        </div>
        <div class="col-md-6 col-12">
          <RouterLink to="/work/CommandCenterDashboard" class="text-decoration-none work-link">
            <div class="work-image-wrap">
              <img
                src="/Work_Overview/CommandCenterDashboard.jpg"
                alt="work-img-3"
                class="img-fluid work-img"
              />
            </div>
            <div class="tag pt-8" @click.stop>
              <span class="button border border-1 border-success text-success lh-170 me-3">
                Cross Platform
              </span>
              <span class="button border border-1 border-success text-success lh-170">
                Dashboard
              </span>
            </div>
            <h3 class="text-success fs-8 lh-170 fw-medium pt-4 pb-3 m-0">能源戰情系統展示牆</h3>
            <p class="lh-170">
              呈現公司在亞太地區的能源佈局與營運績效，設計重點在於資訊整合與視覺化。幫助決策者快速掌握多區域數據，也可直觀展示公司營運實績與競爭優勢。
            </p>
          </RouterLink>
        </div>
        <div class="col-md-6 col-12">
          <RouterLink to="/work/platformRedesign" class="text-decoration-none work-link">
            <div class="work-image-wrap">
              <img
                src="/Work_Overview/PlatformRedesign.jpg"
                alt="work-img-4"
                class="img-fluid work-img"
              />
            </div>
            <div class="tag pt-8" @click.stop>
              <span class="button border border-1 border-success text-success lh-170 me-3">
                Web
              </span>
              <span class="button border border-1 border-success text-success lh-170">
                Redesign
              </span>
            </div>
            <h3 class="text-success fs-8 lh-170 fw-medium pt-4 pb-3 m-0">綠電平台視覺與架構優化</h3>
            <p class="lh-170">
              此次改版聚焦於媒合購售電雙方的流程設計，並改善原有系統的使用痛點，重整資訊架構與介面視覺，打造更直覺、符合內部工作流程的使用體驗。
            </p>
          </RouterLink>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
/* 固定背景圖層 */
.fixed-bg {
  position: fixed;
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
.transparent-animation-bg {
  width: 85%;
  height: 100%;
  overflow: visible;
}
.relative {
  position: relative;
  z-index: 10;
  padding-bottom: 148px;
}
.button {
  border-radius: 100px;
  padding: 6px 20px;
  font-size: 12px;
}
.work-img {
  width: 100%;
  object-fit: cover;
  display: block;
  transition: transform 280ms ease;
}
.work-image-wrap {
  overflow: hidden;
  border-radius: 12px;
  transition: box-shadow 280ms ease;
}
.work-link:hover .work-img,
.work-link:focus-visible .work-img,
.work-link:active .work-img {
  transform: scale(1.08);
}
.work-link:hover .work-image-wrap,
.work-link:focus-visible .work-image-wrap,
.work-link:active .work-image-wrap {
  box-shadow: 0 10px 24px rgba(37, 38, 45, 0.16);
}
p {
  color: #25262d;
}
.tag {
  cursor: default; /* 不顯示手指箭頭 */
}
</style>
