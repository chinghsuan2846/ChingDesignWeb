<script setup>
import CustomButton from '@/components/Button.vue'
import { useBreakpoint } from '@/composables/useBreakpoint'
import TransparentAnimation from '@/components/TransparentAnimation.vue'
import { RouterLink } from 'vue-router'
const { isXs, isSm } = useBreakpoint()
const baseUrl = import.meta.env.BASE_URL
const userAgent = navigator.userAgent
const useTransparentAnimation = /iPad|iPhone|iPod/.test(userAgent) ||
  (navigator.platform === 'MacIntel' && navigator.maxTouchPoints > 1) ||
  (/Safari/i.test(userAgent) && !/Chrome|CriOS|Android/i.test(userAgent))
</script>

<template>
  <div class="page-wrapper background">
    <!-- 固定背景圖 -->
    <div class="fixed-bg d-flex justify-content-start align-items-center">
      <TransparentAnimation
        v-if="useTransparentAnimation"
        animation-path="Globe/HomeAnimation/HomeAnimation.json"
        preserve-aspect-ratio="xMinYMid slice"
        class="transparent-animation-bg"
      />
      <video
        v-else
        autoplay
        muted
        loop
        playsinline
        webkit-playsinline
        preload="auto"
        :poster="`${baseUrl}Home/BG_Image.svg`"
      >
        <source :src="`${baseUrl}Globe/HomeAnimation/chromeAnimation.webm`" type="video/webm" />
        <source :src="`${baseUrl}Globe/HomeAnimation/iOSAnimation.mov`" type="video/quicktime" />
      </video>
    </div>

    <!-- 滿版內容區塊 -->
    <section class="full-height-section">
      <div class="container">
        <div class="row">
          <section class="col-md-8 offset-md-4 col-12 p-0 home-hero">
            <div class="home-text w-100 h-100">
              <h2 class="lh-120 fw-normal fs-1 text-success text-center">CHING DESIGN</h2>
            </div>
          </section>
          <section class="col-lg-7 offset-lg-5 col-12 p-0 py-20 col-12">
            <div class="content w-100 h-100">
              <div v-if="isSm() || isXs()" class="content-bg">
                <div class="content-text d-flex flex-column align-items-center h-100">
                  <h3 class="fw-medium fs-3 text-dark pb-12 pt-11">Work</h3>
                  <div class="pb-10">
                    <RouterLink to="/work/lineLiff" class="home-work-link">
                      <img src="/Home/sticker-1.png" alt="貼紙一" class="sticker-sm-1" />
                    </RouterLink>
                  </div>
                  <div class="pb-10">
                    <RouterLink to="/work/chargingStation" class="home-work-link">
                      <img src="/Home/sticker-2.png" alt="貼紙二" class="sticker-sm-2" />
                    </RouterLink>
                  </div>
                  <div class="pb-10">
                    <RouterLink to="/work/commandCenterDashboard" class="home-work-link">
                      <img src="/Home/sticker-3.png" alt="貼紙三" class="sticker-sm-3" />
                    </RouterLink>
                  </div>
                  <div class="pb-10">
                    <RouterLink to="/work/platformRedesign" class="home-work-link">
                      <img src="/Home/sticker-4.png" alt="貼紙四" class="sticker-sm-4" />
                    </RouterLink>
                  </div>
                  <div class="pb-16">
                    <RouterLink to="/work">
                      <CustomButton> 查看更多 </CustomButton>
                    </RouterLink>
                  </div>
                </div>
              </div>
              <div v-else class="content-bg">
                <div
                  class="content-text d-flex flex-column justify-content-center align-items-center h-100"
                >
                  <h3 class="fw-medium fs-3 text-dark pb-12 pt-4">Work</h3>

                  <RouterLink to="/work">
                    <CustomButton> 查看更多 </CustomButton>
                  </RouterLink>
                </div>
                <img src="/Home/BG_Stroke.svg" alt="背景曲線" class="img-overlay img-fluid" />

                <RouterLink to="/work/lineLiff" class="home-work-link">
                  <img src="/Home/sticker-1.png" alt="貼紙一" class="sticker-1" />
                </RouterLink>
                <RouterLink to="/work/chargingStation" class="home-work-link">
                  <img src="/Home/sticker-2.png" alt="貼紙二" class="sticker-2" />
                </RouterLink>
                <RouterLink to="/work/commandCenterDashboard" class="home-work-link">
                  <img src="/Home/sticker-3.png" alt="貼紙三" class="sticker-3" />
                </RouterLink>
                <RouterLink to="/work/platformRedesign" class="home-work-link">
                  <img src="/Home/sticker-4.png" alt="貼紙四" class="sticker-4" />
                </RouterLink>
              </div>
            </div>
          </section>
          <section class="col-lg-7 offset-lg-5 col-12 p-0 py-20 col-12">
            <div class="content w-100 h-100">
              <div
                v-if="isXs() || isSm()"
                class="content-bg d-flex align-items-center justify-content-center flex-column py-16"
              >
                <div
                  class="personal-card bg-danger border border-1 border-secondary py-14 px-8 mb-20 d-flex flex-column align-items-center"
                >
                  <img
                    src="/Home/Avtar.svg"
                    alt="大頭貼"
                    class="personal-card-img img-fluid pb-6"
                  />
                  <h4 class="text-success fw-medium fs-7">Profile</h4>
                  <hr class="pb-6" />
                  <p>
                    目前是一位 UI/UX
                    設計師，擅長將抽象需求轉化為具體的互動流程與介面設計，能兼顧使用體驗與視覺表現，並在限制中找到符合產品定位的解法。
                  </p>
                </div>
                <RouterLink to="/profile">
                  <CustomButton> 查看更多 </CustomButton>
                </RouterLink>
              </div>

              <div
                v-else
                class="content-bg d-flex align-items-center justify-content-center flex-column"
              >
                <div
                  class="personal-card d-flex bg-danger border border-1 border-secondary py-20 px-12 mb-20"
                >
                  <img
                    src="/Home/Avtar.svg"
                    alt="大頭貼"
                    class="personal-card-img img-fluid pe-12"
                  />
                  <div class="information">
                    <h4 class="text-success fw-medium fs-7">Profile</h4>
                    <hr />
                    <p>
                      目前是一位 UI/UX
                      設計師，擅長將抽象需求轉化為具體的互動流程與介面設計，能兼顧使用體驗與視覺表現，並在限制中找到符合產品定位的解法。
                    </p>
                  </div>
                </div>
                <RouterLink to="/profile">
                  <CustomButton> 查看更多 </CustomButton>
                </RouterLink>
              </div>
            </div>
          </section>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
.page-wrapper {
  padding-top: 80px;
  position: relative;
  overflow: hidden;
}

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

.fixed-bg video,
.fixed-bg .transparent-animation-bg {
  width: 85%;
  height: 100%;
  overflow: visible;
}

/* 整區撐滿視窗 */
.full-height-section {
  position: relative;
  z-index: 10;
}
.home-text {
  padding: 305px 0%;
}
.content {
  width: 60%;
  min-height: 80vh;
  max-height: 100vh;
}
.content-bg {
  background-color: white;
  width: 100%;
  height: 100%;
  background-image: url('/Home/BG_Gird.svg');
  background-size: cover;
  background-position: center;
  position: relative;
  z-index: 20;
  border-radius: 12px;
}
@media (max-width: 768px) {
  .content {
    width: 90%; /* 手機可以撐到更寬，或者 100% */
    min-height: auto; /* 解除固定最小高度 */
    max-height: none; /* 解除最大高度限制 */
  }

  .content-bg {
    height: auto; /* 背景容器跟著內容高度撐開 */
  }
}
.img-overlay {
  position: absolute;
  top: 10%;
  left: 10%;
  width: 80%;
  object-fit: contain;
  pointer-events: none;
  z-index: 21;
  transform: rotate(-4.45deg);
}
.content-text {
  position: relative;
  z-index: 22;
}
.sticker-1 {
  position: absolute;
  width: 40%;
  top: 4%;
  left: 6%;
  z-index: 22;
  transition: transform 0.3s ease;
}
.sticker-sm-1 {
  width: 50%;
  margin-left: auto;
  margin-right: auto;
  transition: transform 0.3s ease;
}
.sticker-1:hover,
.sticker-sm-1:hover,
.home-work-link:hover .sticker-1,
.home-work-link:hover .sticker-sm-1,
.home-work-link:focus-within .sticker-1,
.home-work-link:focus-within .sticker-sm-1,
.home-work-link:active .sticker-1,
.home-work-link:active .sticker-sm-1 {
  transform: rotate(-15deg) scale(1.05);
}
.sticker-2 {
  position: absolute;
  width: 40%;
  top: 4%;
  right: 6%;
  z-index: 22;
  rotate: 10deg;
  transition: transform 0.3s ease;
}
.sticker-sm-2 {
  width: 50%;
  margin-left: auto;
  margin-right: auto;
  rotate: 10deg;
  transition: transform 0.3s ease;
}
.sticker-2:hover,
.sticker-sm-2:hover,
.home-work-link:hover .sticker-2,
.home-work-link:hover .sticker-sm-2,
.home-work-link:focus-within .sticker-2,
.home-work-link:focus-within .sticker-sm-2,
.home-work-link:active .sticker-2,
.home-work-link:active .sticker-sm-2 {
  transform: rotate(-15deg) scale(1.05);
}
.sticker-3 {
  position: absolute;
  width: 45%;
  bottom: 10%;
  left: 7%;
  z-index: 22;
  transition: transform 0.3s ease;
  rotate: 8deg;
}
.sticker-sm-3 {
  width: 50%;
  margin-left: auto;
  margin-right: auto;
  transition: transform 0.3s ease;
  rotate: 8deg;
}
.sticker-3:hover,
.sticker-sm-3:hover,
.home-work-link:hover .sticker-3,
.home-work-link:hover .sticker-sm-3,
.home-work-link:focus-within .sticker-3,
.home-work-link:focus-within .sticker-sm-3,
.home-work-link:active .sticker-3,
.home-work-link:active .sticker-sm-3 {
  transform: rotate(-15deg) scale(1.05);
}
.sticker-4 {
  position: absolute;
  width: 35%;
  bottom: 7%;
  right: 6%;
  z-index: 22;
  transition: transform 0.3s ease;
  rotate: -10deg;
}
.sticker-sm-4 {
  width: 50%;
  margin-left: auto;
  margin-right: auto;
  transition: transform 0.3s ease;
  rotate: -10deg;
}
.sticker-4:hover,
.sticker-sm-4:hover,
.home-work-link:hover .sticker-4,
.home-work-link:hover .sticker-sm-4,
.home-work-link:focus-within .sticker-4,
.home-work-link:focus-within .sticker-sm-4,
.home-work-link:active .sticker-4,
.home-work-link:active .sticker-sm-4 {
  transform: rotate(15deg) scale(1.05);
}
.personal-card {
  max-width: 70%;
  border-radius: 12px;
  transform: rotate(8deg);
  animation: floatUpDown 2s ease-in-out infinite;
}
.personal-card hr {
  align-self: stretch; /* 在 flex container 裡拉滿寬 */
}
@media (max-width: 768px) {
  .personal-card {
    width: 60%; /* 手機可以撐到更寬，或者 100% */
  }
}

@media (max-width: 520px) {
  .personal-card {
    width: 70%; /* 手機可以撐到更寬，或者 100% */
  }
}

/* 平板首頁：以 768px 參考版面維持完整的卡片構圖 */
@media (min-width: 768px) and (max-width: 991.98px) {
  .full-height-section > .container {
    width: 100%;
    max-width: none;
    padding-left: 0;
    padding-right: 0;
  }

  .full-height-section > .container > .row {
    margin-left: 0;
    margin-right: 0;
  }

  .full-height-section > .container > .row > section:first-child {
    flex: 0 0 100%;
    width: 100%;
    max-width: 100%;
    margin-left: 0;
  }

  .full-height-section > .container > .row > section:nth-child(n + 2) {
    padding-left: 0 !important;
    padding-right: 0 !important;
    padding-top: 12px !important;
    padding-bottom: 12px !important;
  }

  .full-height-section > .container > .row > section:nth-child(3) {
    padding-bottom: 120px !important;
  }

  .home-hero {
    height: 751px;
  }

  .fixed-bg video,
  .fixed-bg .transparent-animation-bg {
    width: 100%;
  }

  .content {
    width: calc(100% - 48px) !important;
    height: 690px !important;
    min-height: 690px !important;
    max-height: none !important;
    margin-left: auto;
    margin-right: auto;
  }

  .content-bg {
    height: 100% !important;
  }

  .sticker-1 {
    top: 10%;
    left: 7%;
  }

  .sticker-2 {
    top: 10%;
    right: 7%;
  }

  .sticker-3 {
    bottom: 10%;
    left: 7%;
  }

  .sticker-4 {
    bottom: 8%;
    right: 7%;
  }

  .personal-card {
    width: 74%;
    max-width: 74%;
  }
}

.personal-card-img {
  max-width: 170px;
  max-height: 170px;
}
@keyframes floatUpDown {
  0% {
    transform: translateY(0) rotate(8deg);
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  }
  50% {
    transform: translateY(-10px) rotate(8deg);
    box-shadow: 0 12px 20px rgba(0, 0, 0, 0.1);
  }
  100% {
    transform: translateY(0) rotate(8deg);
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  }
}

/* 平板與手機：讓動畫成為 Hero 背景，標題疊在動畫上方 */
@media (max-width: 991.98px) {
  .fixed-bg {
    position: absolute;
    top: 0;
    height: calc(80px + clamp(653px, 94.7vw, 727px));
    align-items: flex-start;
  }

  .fixed-bg video,
  .fixed-bg .transparent-animation-bg {
    width: 100%;
    height: 100%;
  }

  .fixed-bg video {
    object-fit: cover;
    object-position: 10% center;
  }

  .home-hero {
    position: relative;
    height: clamp(653px, 94.7vw, 727px);
  }

  .home-text {
    position: relative;
    z-index: 12;
    display: flex;
    align-items: flex-start;
    justify-content: center;
    height: 100% !important;
    padding: clamp(150px, 24.5vw, 188px) 0 0 !important;
  }

  .home-text h2 {
    margin-bottom: 0;
  }
}

/* 手機：影片再縮小，保留更多背景留白 */
@media (max-width: 767.98px) {
  .fixed-bg {
    height: calc(80px + clamp(520px, 122vw, 560px));
    align-items: flex-end !important;
    overflow: visible;
  }

  .fixed-bg video,
  .fixed-bg .transparent-animation-bg {
    width: min(85%, calc(100% - 32px));
    height: 85%;
    margin-left: auto;
    margin-right: auto;
  }

  .fixed-bg video {
    object-position: 10% center;
  }

  .home-hero {
    height: clamp(520px, 122vw, 560px);
  }

  .full-height-section > .container {
    width: 100%;
    max-width: none;
    padding-left: 16px;
    padding-right: 16px;
  }

  .full-height-section > .container > .row {
    margin-left: 0;
    margin-right: 0;
  }

  .full-height-section > .container > .row > section {
    padding-left: 0 !important;
    padding-right: 0 !important;
  }

  .full-height-section > .container > .row > section:nth-child(n + 2) {
    padding-top: 16px !important;
    padding-bottom: 16px !important;
  }
}

</style>
