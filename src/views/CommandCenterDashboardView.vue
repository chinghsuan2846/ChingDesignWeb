<template>
  <WorkHead
    title="能源戰情系統展示牆"
    content="透過大螢幕呈現公司在亞太地區的營運佈局與各事業單位實績。介面以清晰直觀的數據視覺化與地理圖像為核心，幫助決策者快速洞察趨勢、優化策略。此外，戰情牆也能作為對外展示工具，協助企業在接待外賓與投資人時，展現完整的營運實力與市場布局。"
    tag="Command Center Dashboard"
    img-url="DashBoard/Title.jpg"
    alt="titleImg"
  />
  <div class="information bg-white">
    <div class="container-xl custom-padding">
      <ProjectInformation
        role="UI/UX 設計師"
        project-duration="2 個月"
        :tools="projectTools"
        :tasks="projectTasks"
      />
      <hr class="mb-12" />
      <ProjectChallenge
        :challenges="projectChallenges"
        img-url="DashBoard/Challenge.png"
        alt="專案挑戰圖"
      />
      <hr class="my-12" />
      <TargetSection :steps="targetSectionSteps" />
      <hr class="my-12" />
      <DesignSystem
        text="資訊與視覺方向"
        content=" 以 國家為層級、台灣細分事業體，視覺風格強調
          專業、科技、簡潔，確保大螢幕展示清晰易讀，同時符合企業形象。"
        img-url1="DashBoard/SiteMap.png"
        alt1="img1"
        img-url2="DashBoard/VisualDirection.png"
        alt2="img2"
      />
      <hr class="my-12" />
      <DesignSystem
        content="設計系統以 深色背景 為主，搭配企業品牌的 藍色與綠色，營造出 專業且具科技感 的氛圍。"
        img-url1="DashBoard/designSystem1.png"
        alt1="designSystem1"
        img-url2="DashBoard/designSystem2.png"
        alt2="designSystem2"
      />
    </div>
  </div>
  <ParallaxSection image="DashBoard/Multiplemockups.svg" class="command-center-parallax" />
  <div class="information">
    <section class="bg-white custom-padding">
      <div>
        <div class="bar-target-interface interface-showcase-first position-relative">
          <div class="bar-line" style="top: 330px">
            <div class="bar-dot-right"></div>
            <div class="bar-line-body-right"></div>
          </div>
          <div class="d-flex justify-content-center pt-16 interface-showcase-heading">
            <BaseDot text="介面展示" class="pb-4" />
          </div>
          <div class="row padding h-100">
            <div class="col-12 col-lg-5 d-flex flex-column interface-copy">
              <h4 class="fw-medium fs-7 pb-5 custom-padding-1 w-100 interface-title">
                <span class="high-light"> 採用 Bento Design，打造彈性模組 </span>
              </h4>
              <div class="w-100 d-flex pb-20 interface-features">
                <div class="d-flex align-items-center me-12">
                  <div class="ring"></div>
                  <span class="ps-3">高度彈性</span>
                </div>
                <div class="d-flex align-items-center me-12">
                  <div class="ring"></div>
                  <span class="ps-3">拼接螢幕友善</span>
                </div>
                <div class="d-flex align-items-center">
                  <div class="ring"></div>
                  <span class="ps-3">多規格適配</span>
                </div>
              </div>
              <p class="interface-description text-start pe-24 me-24 mb-20">
                以便當格形式將戰情資訊拆分為模組，資訊可靈活調整，兼顧拼接螢幕與 Full HD 展示。
              </p>
            </div>
            <div class="col-12 col-lg-7 d-flex position-relative align-items-center interface-visual">
              <picture class="bento-image">
                <source media="(max-width: 390px)" srcset="/DashBoard/bento-design-phone.png" />
                <source
                  media="(min-width: 391px) and (max-width: 991.98px)"
                  srcset="/DashBoard/bento-design-tablet.png"
                />
                <img
                  src="/DashBoard/mockup1_BentoDesing.png"
                  alt="interface1"
                  class="img-position-1"
                />
              </picture>
            </div>
          </div>
        </div>
      </div>
    </section>
    <MarqueeText
      class="command-center-marquee"
      content="SMARTER ENERGY ACCESSIBLE GREEN"
    />
    <section class="bg-info pt-12">
      <div>
        <div class="bar-target-interface position-relative">
          <div class="bar-line" style="top: 274px">
            <div class="bar-dot-left"></div>
            <div class="bar-line-body-left"></div>
          </div>
          <div class="row h-100">
            <div class="col-12 col-lg-6 d-flex align-items-center position-relative interface-visual">
              <img
                src="/DashBoard/mockup2_continuity..png"
                alt="interface2"
                class="img-position-2"
              />
            </div>
            <div class="offset-0 offset-lg-1 col-12 col-lg-4 d-flex flex-column align-items-end interface-copy">
              <h4 class="fw-medium fs-7 pb-5 custom-padding-2 interface-title">
                <span class="high-light"> 延續品牌調性，營造科技感戰情牆 </span>
              </h4>
              <p class="interface-description text-end pt-8 ps-10 ms-24 mb-20">
                融入官網的跑馬燈、格紋背景與地圖等品牌元素，延續企業調性，同時營造科技感與專業戰情氛圍。
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="bg-white">
      <div>
        <div class="bar-target-interface position-relative">
          <div class="bar-line" style="top: 285px">
            <div class="bar-dot-right-2"></div>
            <div class="bar-line-body-right-2"></div>
          </div>
          <div class="row justify-content-between h-100">
            <div class="offset-0 offset-lg-1 col-12 col-lg-5 d-flex flex-column align-items-start interface-copy">
              <h4 class="fw-medium fs-7 pb-5 custom-padding-3 ms-2 interface-title">
                <span class="high-light"> 融入動態元素，提升展示吸引力 </span>
              </h4>
              <p class="interface-description text-start pt-8 pe-24 me-24 mb-20">
                為避免戰情牆只呈現靜態資訊，我們加入
                動態元素，如數據變化動畫與焦點高亮，讓內容更生動易讀。在展覽或對外展示時，也能迅速吸引觀眾目光，提升整體互動感與科技感。
              </p>
            </div>
            <div class="col-12 col-lg-6 d-flex align-items-center position-relative interface-visual">
              <video
                src="/DashBoard/mockup3.webm"
                autoplay
                loop
                muted
                playsinline
                class="interface-video"
              ></video>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="bg-info">
      <div>
        <div class="d-flex justify-content-center pt-16">
          <BaseDot text="前後版本對比" class="pb-4" />
        </div>
        <div class="container d-flex justify-content-center">
          <p class="text-center custom-width lh-170">
            原本版本風格較傳統簡潔，資訊未經歸納整理，閱讀時容易分散注意力。新的版本則採
            創新設計風格，延續品牌一致性，並融入 動態元素 提升吸引力。同時以
            模組化方式呈現資訊，讓內容更清晰易讀，使用者能快速掌握關鍵數據。
          </p>
        </div>
        <div class="w-100 custom-padding-bottom">
          <BeforeAfterSlider
            beforeImg="DashBoard/mockup4_before.png"
            afterImg="DashBoard/mockup4_after.png"
            class="dashboard-before-after"
          />
        </div>
      </div>
    </section>
  </div>
  <ResultSection
    content="這次的能源戰情牆專案讓我能思考如何在大型拼接螢幕上有效呈現龐雜資訊，同時兼顧視覺美感與品牌一致性。透過 Bento Design 模組化思維讓內容具備高度彈性，不僅解決了多螢幕展示的挑戰，也為未來延伸至不同裝置或展示場域打下基礎。也在這個專案中體會到設計在資訊整合與品牌價值傳遞上的關鍵角色。"
  />
  <OthersWorkSection
    img-url1="Work_Overview/ChargingStationDSSDesign.jpg"
    alt1="ChargingStationDSSDesign"
    route1="/work/chargingStation"
    img-url2="Work_Overview/PlatformRedesign.jpg"
    alt2="PlatformRedesign"
    route2="/work/platformRedesign"
  />
</template>

<style scoped>
p {
  line-height: 170%;
  color: #25262d;
}
.information {
  width: 100%;
  position: relative;
  border-radius: 40px;
  z-index: 10;
  overflow: hidden;
}
.custom-rounded {
  padding: 6.5px 20px;
  border-radius: 100px;
}
.custom-rounded-2 {
  padding: 4.5px 24px;
  border-radius: 38px;
}
.custom-padding {
  padding: 60px;
}
.text-bar {
  display: block;
  width: 4px;
  background-color: #eaf0f6;
  margin-right: 12px;
}
.img-padding {
  padding-left: 80px;
  object-fit: cover;
}
.task-flow-img {
  border-radius: 10px;
}
.menu-img {
  border-radius: 10px;
  padding: 64px 32px;
}
.site-map-img {
  border-radius: 10px;
  padding: 35px 86px;
}
.high-light {
  position: relative;
  z-index: 1;
}
.high-light::before {
  content: '';
  position: absolute;
  top: 50%;
  left: -0.3em;
  right: 0;
  width: calc(100% + 0.6em);
  height: 16px;
  background-color: #94ffe1;
  opacity: 0.7;
  z-index: -1; /* 確保在文字後面 */
}
.custom-padding-1 {
  padding-top: 124px;
}
.custom-padding-2 {
  padding-top: 220px;
}
.custom-padding-3 {
  padding-top: 225px;
}

.bar-target-interface {
  overflow: hidden;
  height: 635px;
}
.bar-line {
  position: absolute;
  left: 0;
  width: 100%;
  pointer-events: none; /* 不要影響點擊 */
  z-index: 5;
}
.bar-dot-right {
  position: absolute;
  right: 60%;
  width: 6px;
  height: 6px;
  background-color: #769bd9;
  border-radius: 50%;
  transform: translateX(50%);
  top: 0;
}
.bar-line-body-right {
  position: absolute;
  right: 60%;
  width: 75%;
  height: 1px;
  background-color: #769bd9;
  top: 2.5px;
}
.bar-dot-left {
  position: absolute;
  left: 35.8%;
  width: 6px;
  height: 6px;
  background-color: #769bd9;
  border-radius: 50%;
  transform: translateX(-50%);
  top: 0;
}
.bar-line-body-left {
  position: absolute;
  left: 35.8%;
  width: 54%;
  height: 1px;
  background-color: #769bd9;
  top: 2.5px;
}
.bar-line-body-right-2 {
  position: absolute;
  right: 37.6%;
  width: 54%;
  height: 1px;
  background-color: #769bd9;
  top: 2.5px;
}
.bar-dot-right-2 {
  position: absolute;
  right: 37.6%;
  width: 6px;
  height: 6px;
  background-color: #769bd9;
  border-radius: 50%;
  transform: translateX(50%);
  top: 0;
}
.img-position-1 {
  position: absolute;
  top: -3%;
  left: -4%;
  z-index: 1;
  max-width: 100%; /* 以 col-6 為基準縮放 */
}
.img-position-2 {
  position: absolute;
  left: -1.5%;
  z-index: 1;
  max-width: 100%; /* 以 col-6 為基準縮放 */
}
.ring {
  width: 13px;
  height: 13px;
  border-radius: 50%;
  background: linear-gradient(to bottom, #81a3dc, #d4dff2); /* 上深下淺 */
  -webkit-mask: radial-gradient(circle, transparent 40%, black 41%); /* 中間挖空 */
  mask: radial-gradient(circle, transparent 40%, black 41%);
}
.padding {
  padding-top: 18px;
}
.custom-width {
  width: 78%;
}
.custom-padding-bottom {
  padding-bottom: 80px;
}
.interface-title {
  width: 100%;
}
.interface-video {
  display: block;
  max-width: 100%;
  height: auto;
}

@media (max-width: 991.98px) {
  /* Keep the same page gutter as the other responsive case studies. */
  .information > .container-xl.custom-padding {
    padding: 60px 24px;
  }

  .information > section.custom-padding,
  .information > section:not(.custom-padding) {
    padding-left: 24px;
    padding-right: 24px;
  }

  .information > section.custom-padding {
    padding-top: 24px;
    padding-bottom: 24px;
  }

  .bar-target-interface {
    height: auto;
    min-height: 0;
    padding: 48px 0 64px;
  }

  .interface-showcase-first {
    padding-top: 16px;
  }

  .interface-showcase-first .interface-showcase-heading {
    padding-top: 24px !important;
  }

  .bar-target-interface > .row {
    height: auto !important;
    margin-left: 0;
    margin-right: 0;
    padding-top: 0;
  }

  .bar-target-interface > .row > .interface-copy,
  .bar-target-interface > .row > .interface-visual {
    width: 100%;
    max-width: 100%;
    flex: 0 0 auto;
  }

  .bar-target-interface > .row > .interface-copy {
    order: 1;
    align-items: center !important;
  }

  .bar-target-interface > .row > .interface-visual {
    order: 2;
    justify-content: center;
    padding-left: 0;
    padding-right: 0;
  }

  .bar-target-interface .bar-line {
    display: none;
  }

  .interface-title {
    padding-top: 32px !important;
    padding-bottom: 20px !important;
    margin-left: 0 !important;
    text-align: center;
    white-space: normal;
    font-size: 20px !important;
  }

  .interface-description {
    padding: 0 !important;
    margin: 0 0 8px !important;
    text-align: center !important;
  }

  .interface-features {
    justify-content: center;
    flex-wrap: wrap;
    gap: 16px;
    padding-bottom: 32px !important;
  }

  .interface-features > div {
    margin-right: 0 !important;
  }

  .interface-visual .img-position-1,
  .interface-visual .img-position-2 {
    position: static;
    left: auto;
    right: auto;
    width: 100%;
    max-width: 100%;
    height: auto;
    transform: none;
  }

  .interface-video {
    width: 100%;
  }

  .custom-padding-1,
  .custom-padding-2,
  .custom-padding-3 {
    padding-top: 32px;
  }

  .custom-width {
    width: 100%;
  }

  .custom-padding-bottom {
    padding-bottom: 48px;
  }
}

@media (min-width: 768px) and (max-width: 991.98px) {
  .interface-title {
    white-space: nowrap;
  }
}

@media (max-width: 390px) {
  .command-center-parallax :deep(.parallax-background) {
    height: 100%;
    top: 0;
  }

  .interface-title {
    font-size: 18px !important;
    letter-spacing: -0.08em;
    white-space: nowrap;
  }

  .interface-title .high-light {
    letter-spacing: inherit;
  }

  .interface-features {
    flex-wrap: nowrap;
    gap: 0;
    justify-content: space-between;
  }

  .interface-features > div {
    flex: 0 1 auto;
  }

  .interface-features .ring {
    width: 12px;
    height: 12px;
  }

  .interface-features span {
    padding-left: 4px !important;
    font-size: 14px;
    white-space: nowrap;
  }

  .interface-visual > .bento-image {
    display: block;
    width: 100%;
  }

  .dashboard-before-after :deep(.slider-container) {
    width: 96%;
  }

  .interface-description {
    font-size: 14px;
    margin-bottom: 8px !important;
  }
}
</style>

<script setup>
import BaseDot from '@/components/Dot.vue'
import WorkHead from '@/components/WorkHead.vue'
import ProjectInformation from '@/components/ProjectInformation.vue'
import ProjectChallenge from '@/components/ProjectChallenge.vue'
import TargetSection from '@/components/TargetSection.vue'
import DesignSystem from '@/components/DesignSystem.vue'
import ParallaxSection from '@/components/ParallaxSection.vue'
import ResultSection from '@/components/ResultSection.vue'
import OthersWorkSection from '@/components/OthersWorkSection.vue'
import MarqueeText from '@/components/MarqueeText.vue'
import BeforeAfterSlider from '@/components/BeforeAfterSlider.vue'

const projectTools = ['Figma', 'Illustrator', 'After Effect']

const projectTasks = ['視覺提案', 'UI Mockup', 'UI Hand-off']

const projectChallenges = [
  {
    title: '硬體限制 : 4x2 拼接螢幕',
    content: '必須符合 4x2 拼接螢幕 的展示需求，確保跨螢幕之間的資訊布局具備連貫性與一致性。',
  },
  {
    title: '內容彈性',
    content: '戰情資訊需因應不同策略調整顯示內容與數據，因此系統必須設計成可靈活更新的網站架構。',
  },
  {
    title: '特殊尺寸適配',
    content: '需同時支援 4x2 拼接螢幕 與 Full HD 螢幕 的顯示，確保不同展示環境下的使用體驗一致。',
  },
]

const targetSectionSteps = [
  {
    stepNum: '01',
    title: '拼接螢幕體驗最佳化',
    content:
      '針對 4x2 拼接螢幕設計資訊排布，確保跨螢幕視覺連貫與整體一致性，提供清晰流暢的閱讀體驗。',
    img: 'DashBoard/target1_Screen.svg',
    alt: 'screen',
  },
  {
    stepNum: '02',
    title: '靈活的資訊架構',
    content: '建立模組化與可擴充的設計系統，讓戰情資訊能隨策略變動快速更新，保持介面清晰穩定。',
    img: 'DashBoard/target2_Architecture.svg',
    alt: 'target2_Architecture',
  },
  {
    stepNum: '03',
    title: '雙規格展示適配',
    content: '設計同時支援拼接螢幕與 Full HD 螢幕，讓資訊在不同展示場域都能精準傳達。',
    img: 'DashBoard/target2_DoubleScreen.svg',
    alt: 'DoubleScreen',
  },
]
</script>
