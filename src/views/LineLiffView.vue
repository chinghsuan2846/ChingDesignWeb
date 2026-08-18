<template>
  <WorkHead
    title="星舟快充 LINE Liff 設計"
    content="星舟快充是一家提供電動車充電站服務的營運商。由於當前的電動車充電操作大多依賴手機應用，本專案針對其官方LINE 帳號進行 2.0 版本改版，目標是優化介面設計，提升操作便利性與整體用戶體驗。"
    tag="LINE Liff Design"
    img-url="LINELiff/MainVision.jpg"
    alt="主圖"
  />
  <div class="information bg-white">
    <div class="container-xl custom-padding">
      <ProjectInformation
        role="UI/UX 設計師"
        project-duration="4 個月"
        :tools="projectTools"
        :tasks="projectTasks"
      />
      <hr class="mb-12" />
      <ProjectChallenge
        :challenges="projectChallenges"
        img-url="LINELiff/Challenge.png"
        alt="專案挑戰圖"
      />
      <hr class="my-12" />
      <TargetSection :steps="targetSectionSteps" />
      <hr class="my-12" />
      <div class="row task-flow-row justify-content-between align-items-center g-0">
        <div class="col-7 task-flow-main">
          <img
            src="/LINELiff/TaskFlow.png"
            alt="任務流程圖"
            class="img-fluid task-flow-img border border-1 p-12 bg-light"
          />
        </div>

        <div class="col-2 d-flex justify-content-center task-flow-arrow">
          <img src="/LINELiff/Arrow.svg" alt="箭頭" />
        </div>

        <div class="col-3 task-flow-menu d-flex justify-content-center">
          <img
            src="/LINELiff/Menu.png"
            alt="選單"
            class="img-fluid menu-img border border-1 bg-light"
          />
        </div>
      </div>

      <hr class="my-12" />
      <QuestionSection
        content="透過使用流程的分析，我們發現部分操作不夠直覺，功能安排也沒完全符合使用者在充電時的實際需求，這成為後續優化的重點。"
        :questions="questionDefineQuestions"
      />
      <hr class="my-12" />
      <InformationArchitecture
        content="根據前階段對任務流程的梳理與問題定義，我們重新規劃了頁面結構與功能配置。"
        img-url="LINELiff/SiteMap.png"
        alt="資訊架構圖"
      />
      <hr class="my-12" />
      <DesignSystem
        content="採用 Material Design 建立具延展性的設計系統，搭配深色視覺，營造品牌穩重與信任感，同時展現科技形象。"
        img-url1="LINELiff/Guideline1.png"
        alt1="guideline1"
        img-url2="LINELiff/Guideline2.png"
        alt2="guideline2"
      />
    </div>
  </div>
  <ParallaxSection image="LINELiff/Multiple mockups.svg" />
  <div class="information">
    <section class="bg-white p-23">
      <div class="container-xl">
        <div class="bar-target-mockup2 position-relative">
          <div class="d-flex justify-content-center">
            <BaseDot text="介面展示" class="pb-4" />
          </div>
          <div class="row flex-lg-row-reverse">
            <div class="col-12 col-lg-6 d-flex flex-column align-items-center align-items-lg-end">
              <h4 class="fw-medium fs-8 pb-5 custom-padding-2 interface-title">
                <span class="high-light"> 快速掌握最近充電站，輕鬆回訪充電足跡！ </span>
              </h4>
              <p class="interface-description text-center text-lg-end pt-lg-4">
                介面除了能即時查看附近可用的充電站外，搜尋欄也會記錄使用者過去使用過的站點，方便快速選取，提升整體操作效率。
              </p>
            </div>
            <div class="col-12 col-lg-6 position-relative">
              <div class="bar-line d-none d-lg-block" style="top: 33%">
                <div class="bar-dot-left"></div>
                <div class="bar-line-body-left"></div>
              </div>
              <div class="d-flex align-items-center">
                <img src="/LINELiff/Mockup1.png" alt="mockup1" class="img-position-1" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="bg-info px-23">
      <div class="container-xxl">
        <div class="bar-target-mockup1 position-relative">
          <div class="row">
            <div class="col-12 col-lg-6 d-flex flex-column align-items-center align-items-lg-start">
              <h4 class="fw-medium fs-8 pb-5 custom-padding-1 interface-title">
                <span class="high-light"> 即時掌握充電空位，預約無憂，告別撲空！ </span>
              </h4>
              <p class="interface-description text-center text-lg-start pt-xl-8 pe-lg-20 me-lg-20">
                介面整合即時充電樁狀態查詢與預約功能，使用者可一眼掌握空位情況，避免白跑，也能提前預約，提升整體充電效率與掌控感。
              </p>
            </div>
            <div class="col-12 col-lg-6 position-relative">
              <div class="img-wrapper custom-img-container">
                <div class="bar-line d-none d-lg-block" style="top: 45%">
                  <div class="bar-dot-right"></div>
                  <div class="bar-line-body-right"></div>
                </div>
                <img src="/LINELiff/Mockup2.png" alt="mockup2" class="img-position-2" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="bg-white px-23">
      <div class="container-xl">
        <div class="bar-target-mockup3 position-relative">
          <div class="row flex-lg-row-reverse">
            <div class="col-12 col-lg-6 d-flex flex-column align-items-center align-items-lg-end">
              <h4 class="fw-medium fs-8 pb-5 custom-padding-3 interface-title">
                <span class="high-light"> 隨時掌握充電進度，行程無縫順行！</span>
              </h4>
              <p class="interface-description text-center text-lg-end pt-lg-4 ps-lg-20 ms-lg-20">
                介面提供即時充電進度回報，使用者可隨時查看目前充電狀態，搭配充電完成通知，讓行程安排更有彈性也更安心。
              </p>
            </div>

            <div class="col-12 col-lg-6 position-relative">
              <div class="img-wrapper wrapper-3">
                <div class="bar-line d-none d-lg-block" style="top: 45%">
                  <div class="bar-dot-left-2"></div>
                  <div class="bar-line-body-left-2"></div>
                </div>
                <img src="/LINELiff/Mockup3.png" alt="mockup3" class="img-position-3" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="bg-info px-23">
      <div class="container-xl py-16">
        <div class="bar-target-mockup4 position-relative overflow-hidden">
          <div class="row">
            <div class="col-12 col-lg-6 d-flex flex-column align-items-center align-items-lg-start">
              <h4 class="fw-medium fs-8 pb-5 custom-padding-4 interface-title">
                <span class="high-light"> 智慧分析充電支出，輕鬆掌握用電成本！ </span>
              </h4>
              <p class="interface-description text-center text-lg-start pt-xl-8 pe-lg-20 me-lg-20">
                系統整合充電紀錄與金額統計，讓使用者能清楚掌握每次充電的支出與用電趨勢，協助更有效地管理用電成本。
              </p>
            </div>
            <div class="col-12 col-lg-6 position-relative">
              <div class="bar-line d-none d-lg-block" style="top: 39%">
                <div class="bar-dot-right-2"></div>
                <div class="bar-line-body-right-2"></div>
              </div>
              <div class="d-flex justify-content-center justify-content-lg-end">
                <img src="/LINELiff/Mockup4.png" alt="mockup4" class="img-position-4" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>

  <ResultSection
    content="在製作這個專案的過程中，我們不僅要解決充電站搜尋、預約與費用管理等痛點，還面臨了必須透過
        LINE LIFF 頁面呈現的挑戰。與市面上的獨立 APP 不同，LIFF限制了即時通知與背景更新功能，需要透過更精簡的介面設計來提升使用體驗，確保資訊清晰、操作流暢。儘管過程充滿挑戰，但希望能讓電動車主的充電體驗更加流暢便捷！"
  />
  <OthersWorkSection
    img-url1="Work_Overview/PlatformRedesign.jpg"
    alt1="PlatformRedesign"
    route1="/work/platformRedesign"
    img-url2="Work_Overview/ChargingStationDSSDesign.jpg"
    alt2="ChargingStationDSSDesign"
    route2="/work/chargingStation"
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
.information {
  width: 100%;
  position: relative;
  border-radius: 40px;
  z-index: 10;
  background-color: #fff; /* 假設你的背景是白色 */
}

.custom-padding {
  padding: 60px 0;
}

.img-padding {
  padding-left: 80px;
  object-fit: cover;
}
.task-flow-img {
  border-radius: 10px;
}
@media (min-width: 375px) and (max-width: 768px) {
  .task-flow-row {
    flex-direction: column;
    align-items: center;
  }

  .task-flow-main,
  .task-flow-arrow,
  .task-flow-menu {
    width: 100%;
    max-width: 100%;
    text-align: center;
  }

  .task-flow-main {
    margin-bottom: 24px;
  }

  .task-flow-arrow {
    margin-bottom: 24px;
  }

  .task-flow-menu {
    margin-bottom: 0;
  }

  /* 箭頭轉向 ↓ */
  .task-flow-arrow img {
    transform: rotate(90deg);
  }
}

.menu-img {
  border-radius: 10px;
  padding: 64px 32px;
}
.high-light {
  background: linear-gradient(180deg, transparent 50%, #ffd194 50%);
  box-decoration-break: clone;
  padding: 0 0.3em;
  display: inline;
}

.custom-padding-1 {
  padding-top: 64px;
}
.custom-padding-3 {
  padding-top: 64px;
}

.custom-padding-4 {
  padding-top: 64px;
}
@media (min-width: 992px) {
  .custom-padding-2 {
    padding-top: 19%;
  }
  .custom-padding-1 {
    padding-top: 43%;
  }
  .custom-padding-3 {
    padding-top: 37%;
  }
  .custom-padding-4 {
    padding-top: 29%;
  }
  .custom-padding-2,
  .custom-padding-3,
  .custom-padding-4 {
    white-space: nowrap;
  }
}
.custom-padding-5 {
  padding: 100px 176px;
}

.bar-target-mockup2 {
  overflow: hidden;
  height: auto;
}

.bar-target-mockup2::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 200px;
  pointer-events: none;
  background: linear-gradient(to bottom, rgba(255, 255, 255, 0), #fff);
  z-index: 10;
}
.bar-target-mockup3 {
  overflow: hidden;
  height: auto;
}
.bar-target-mockup3::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 200px;
  pointer-events: none;
  background: linear-gradient(to bottom, rgba(255, 255, 255, 0), #fff);
  z-index: 10;
}
.bar-target-mockup1 {
  height: auto;
}
@media (min-width: 992px) {
  .bar-target-mockup1 {
    height: 635px;
  }
  .bar-target-mockup3 {
    height: 635px;
  }
  .bar-target-mockup4 {
    height: 635px;
  }
}
.bar-target-mockup4 {
  height: auto;
}
.img-wrapper {
  overflow: visible; /* ✨ 允許圖片橫向超出 */
}
.bar-line {
  position: absolute;
  left: 0;
  width: 100%;
  pointer-events: none; /* 不要影響點擊 */
  z-index: 5;
}
.bar-dot-left {
  position: absolute;
  left: 65%;
  width: 6px;
  height: 6px;
  background-color: #769bd9;
  border-radius: 50%;
  transform: translateX(-50%);
  top: 0;
}
.bar-line-body-left {
  position: absolute;
  left: 65%;
  width: 150%;
  height: 1px;
  background-color: #769bd9;
  top: 2.5px;
}

.bar-dot-right-2 {
  position: absolute;
  right: 63%;
  width: 6px;
  height: 6px;
  background-color: #769bd9;
  border-radius: 50%;
  transform: translateX(50%);
  top: 0;
}
.bar-line-body-right-2 {
  position: absolute;
  right: 63%;
  width: 150%;
  height: 1px;
  background-color: #769bd9;
  top: 2.5px;
}
.img-position-1 {
  width: 90%;
}
/* 手機版預設 */
.custom-img-container {
  position: static;
  width: auto;
}
.img-position-2 {
  transform: scale(1); /* 恢復原狀 */
}

/* 桌面版（lg 以上）：套用原本的放大與定位 */
@media (min-width: 992px) {
  /* 這個容器負責整體的「定位」與「大小限制」 */
  .custom-img-container {
    position: absolute;
    right: -4%;
    top: 19%;
    width: 100%; /* 寬度跟隨父欄位 */
  }

  /* 只有圖片自己放大，不會影響到線條的粗細 */
  .img-position-2 {
    width: 100%;
    display: block;
    transform: scale(1.45);
    transform-origin: center;
  }

  /* 線條直接定位在 custom-img-container 上 */
  /* 因為 container 沒有被 scale，所以這裡的 1px 永遠是 1px */
  .bar-dot-right {
    position: absolute;
    right: 35%; /* 這裡需要根據放大後的視覺位置微調百分比 */
    width: 6px;
    height: 6px;
    background-color: #769bd9;
    border-radius: 50%;
    transform: translateX(50%);
    top: 0;
    z-index: 2; /* 確保在放大後的圖片上方 */
  }

  .bar-line-body-right {
    position: absolute;
    right: 35%;
    width: 167%;
    height: 1px; /* 這裡會保持精確的 1px */
    background-color: #769bd9;
    top: 2.5px;
    z-index: 2;
  }
}
/* 手機版預設：不放大、居中、static */
.wrapper-3 {
  position: static;
  display: flex;
  justify-content: center;
}

.img-position-3 {
  display: block; /* 消除圖片底部預設的空白間隙 */
  width: 60%; /* 讓圖片填滿寬度 */
  height: auto; /* 確保比例正確 */
  transform: scale(1);
}

/* 桌面版：控制位置與圖片縮放 */
@media (min-width: 992px) {
  .wrapper-3 {
    position: absolute;
    left: 3%; /* 控制整組（含線）在欄位中的位置 */
    top: -40%; /* 根據版面微調高度 */
    width: 100%;
    display: block;
  }

  .img-position-3 {
    width: 100%;
    display: block;
    transform: scale(1.1); /* 只有圖片放大，線條不變粗 */
    transform-origin: center;
  }

  /* 線條定位：因為在 wrapper-3 內且 wrapper 沒 scale，線條維持 1px */
  .bar-dot-left-2 {
    position: absolute;
    left: 96%; /* 這裡請根據圖片放大後的視覺位置調整百分比 */
    width: 6px;
    height: 6px;
    background-color: #769bd9;
    border-radius: 50%;
    transform: translateX(-50%); /* 點的中心對準 left */
    top: 0;
    z-index: 2;
  }

  .bar-line-body-left-2 {
    position: absolute;
    width: 170%;
    left: 96%; /* 連接到點的位置 */
    height: 1px;
    background-color: #769bd9;
    top: 2.5px;
    z-index: 2;
  }
}
.img-position-4 {
  width: 77%;
}

@media (max-width: 991.98px) {
  /* Keep a consistent page gutter when the desktop columns stack. */
  .information > .container-xl.custom-padding {
    padding-left: 24px;
    padding-right: 24px;
  }

  .information > section {
    padding-left: 24px !important;
    padding-right: 24px !important;
  }

  .information > section > .container-xl,
  .information > section > .container-xxl {
    padding-left: 0;
    padding-right: 0;
  }

  .custom-padding-2,
  .custom-padding-3,
  .custom-padding-4 {
    padding-top: 32px;
    white-space: normal;
    text-align: center;
  }

  .bar-target-mockup2::after,
  .bar-target-mockup3::after {
    display: none;
  }

  .bar-target-mockup2,
  .bar-target-mockup3,
  .bar-target-mockup4 {
    overflow: visible;
  }
}

.interface-title {
  width: 100%;
}

@media (min-width: 768px) {
  .interface-title {
    white-space: nowrap;
  }
}

@media (max-width: 390px) {
  .interface-title {
    font-size: 18px !important;
    letter-spacing: -0.08em;
    white-space: nowrap;
  }

  .interface-title .high-light {
    letter-spacing: inherit;
  }

  .interface-description {
    font-size: 14px;
  }
}
</style>

<script setup>
import BaseDot from '@/components/Dot.vue'
import WorkHead from '@/components/WorkHead.vue'
import ProjectInformation from '@/components/ProjectInformation.vue'
import ProjectChallenge from '@/components/ProjectChallenge.vue'
import TargetSection from '@/components/TargetSection.vue'
import QuestionSection from '@/components/QuestionSection.vue'
import InformationArchitecture from '@/components/InformationArchitecture.vue'
import DesignSystem from '@/components/DesignSystem.vue'
import ParallaxSection from '@/components/ParallaxSection.vue'
import ResultSection from '@/components/ResultSection.vue'
import OthersWorkSection from '@/components/OthersWorkSection.vue'

const projectTools = ['Figma', 'Illustrator', 'After Effects']

const projectTasks = ['Task Flow', '設計系統', 'UI Mockup', 'UI Hand-off']

const projectChallenges = [
  {
    title: '平台策略 - 優先採用 LINE LIFF',
    content:
      '專案初期基於使用者熟悉度與開發時程考量，選擇以 LINE LIFF 作為平台，需克服 WebView體驗與效能上的限制。',
  },
  {
    title: '設計需具備未來 App 化彈性',
    content:
      '雖然目前為 LIFF頁面，但考量長期產品發展，設計上需保有模組化與系統性，以利未來轉型為原生 App。',
  },
  {
    title: '用戶預期與平台落差',
    content:
      '多數競品為原生 App，使用者對於充電服務的流暢性與穩定性有較高預期，因此需在 LIFF中打造近似原生的使用體驗。',
  },
]

const targetSectionSteps = [
  {
    stepNum: '01',
    title: '打造接近原生 App 的流暢體驗',
    content:
      '透過清晰的資訊架構與簡潔的操作流程，減輕 WebView帶來的延遲感與互動斷層，提升整體使用感受。',
    img: 'LINELiff/mobile icon.svg',
    alt: 'mobile icon',
  },
  {
    stepNum: '02',
    title: '建立具擴展性的設計系統',
    content:
      '考量後續產品可能轉為 App，設計初期即選擇 Material Design為基礎，兼顧行動端支援性與系統延展性。',
    img: 'LINELiff/DesignSystem icon.svg',
    alt: 'Design System icon',
  },
  {
    stepNum: '03',
    title: '簡化操作流程、提升任務完成率',
    content:
      '聚焦核心任務（如查找充電站、啟動充電等）的流程優化，降低首次使用的學習曲線，提高操作直覺性與效率。',
    img: 'LINELiff/task icon.svg',
    alt: 'task icon',
  },
]

const questionDefineQuestions = [
  {
    num: '1',
    title: '選單內容未貼近使用者需求',
    content: '沒有一目了然的充電操作，進到畫面會不知道要先點甚麼',
    img: 'LINELiff/Problem1_menu.svg',
    alt: 'problem1 menu',
  },
  {
    num: '2',
    title: '無法顯示當前最近充電站',
    content: '僅顯示站點列表，無法查看離自己最近的充電站或記錄曾去過的充電站',
    img: 'LINELiff/Problem2_stop.svg',
    alt: 'problem2 stop',
  },
  {
    num: '3',
    title: '無顯示充電空位與預約',
    content: '無法進行充電槍預約，在前往充電站的途中，容易造成使用者等待或撲空',
    img: 'LINELiff/Problem3_reservation.svg',
    alt: 'problem3 reservation',
  },
  {
    num: '4',
    title: '缺乏自動化的統計和分析',
    content: '使用者目前只能以條列方式查看歷史訂單，系統並未提供統計或彙整功能',
    img: 'LINELiff/Problem4_nonAuto.svg',
    alt: 'problem4 nonAuto',
  },
]
</script>
