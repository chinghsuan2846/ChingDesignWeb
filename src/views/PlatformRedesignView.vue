<template>
  <WorkHead
    title="綠電平台視覺與架構優化"
    content="平台在初期開發時，缺乏一致設計。此次專案藉由新系統開發為契機，優化使用者體驗、建立設計系統並改善協作流程，最終成果兼顧跨平台延展性與開發效率，並改善整體操作體驗。"
    tag="Web"
    img-url="PlatformRedesign/title.png"
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
        img-url="PlatformRedesign/challenge.png"
        alt="專案挑戰圖"
      />
      <hr class="my-12" />
      <TargetSection :steps="targetSectionSteps" />
      <hr class="my-12" />
      <QuestionSection
        title="現有痛點"
        content="現有系統痛點包含：操作路徑不清晰、角色與任務定位模糊、流程缺乏指引，以及錯誤回饋不足，導致使用者容易迷失並增加操作成本。"
        :questions="questionDefineQuestions"
      />
      <div class="d-flex justify-content-center align-items-center my-12">
        <img src="/PlatformRedesign/arrow.svg" alt="arrow" />
      </div>
      <BaseDot text="優化目標" class="pb-4" />
      <div class="row mb-12 g-4">
        <div class="col-12 col-md-4 d-flex">
          <div class="card bg-warning border-1 w-100">
            <div class="card-body p-8 w-100">
              <div
                class="d-flex align-items-center justify-content-center border-bottom border-1 border-secondary pb-4"
              >
                <span
                  class="stepNumber fw-bold d-inline-flex justify-content-center align-items-center rounded-circle bg-success text-white lh-170"
                >
                  01
                </span>
                <h4 class="fw-medium lh-170 text-success fs-9 mb-0 ms-3">資訊架構</h4>
              </div>
              <div class="pt-4 text-center">
                <p class="mb-0 lh-170">固定功能位置與色彩區分，幫助快速定位</p>
              </div>
            </div>
          </div>
        </div>
        <div class="col-12 col-md-4 d-flex">
          <div class="card bg-warning border-1 w-100">
            <div class="card-body p-8 w-100">
              <div
                class="d-flex align-items-center justify-content-center border-bottom border-1 border-secondary pb-4"
              >
                <span
                  class="stepNumber fw-bold d-inline-flex justify-content-center align-items-center rounded-circle bg-success text-white lh-170"
                >
                  02
                </span>
                <h4 class="fw-medium lh-170 text-success fs-9 mb-0 ms-3">操作體驗優化</h4>
              </div>
              <div class="pt-4 text-center">
                <p class="mb-0 lh-170">減少資訊負擔，加入明確引導</p>
              </div>
            </div>
          </div>
        </div>
        <div class="col-12 col-md-4 d-flex">
          <div class="card bg-warning border-1 w-100">
            <div class="card-body p-8 w-100">
              <div
                class="d-flex align-items-center justify-content-center border-bottom border-1 border-secondary pb-4"
              >
                <span
                  class="stepNumber fw-bold d-inline-flex justify-content-center align-items-center rounded-circle bg-success text-white lh-170"
                >
                  03
                </span>
                <h4 class="fw-medium lh-170 text-success fs-9 mb-0 ms-3">跨平台一致</h4>
              </div>
              <div class="pt-4 text-center">
                <p class="mb-0 lh-170">統一設計系統，支持未來延展</p>
              </div>
            </div>
          </div>
        </div>
      </div>
      <hr class="my-12" />
      <DesignSystem
        text="視覺方向"
        content="介面樣式使用資料夾外框與點點紙背景，呼應系統的文書與試算性質。設計借用實體物件的熟悉感，降低使用門檻，同時營造溫度與辨識度。"
        img-url1="PlatformRedesign/visualDirection.png"
        alt1="visualDirection"
        img-url2="PlatformRedesign/moodBoard.png"
        alt2="moodBoard"
      />
      <hr class="my-12" />
      <DesignSystem
        text="色彩計畫"
        content="兩個平台以暖、冷色調與紙張質感背景區分；三個角色則配置便條紙般的低彩度色系，並以藏青色作為整體基調。"
        img-url1="PlatformRedesign/colorScheme1.png"
        alt1="colorScheme1"
        img-url2="PlatformRedesign/colorScheme2.png"
        alt2="colorScheme2"
      />
      <hr class="my-12" />
      <DesignSystem
        content="文字部分使用 Noto Sans TC，英文與數字字體使用 Oxanium，現代感強又帶有文書感，能清晰呈現數據資訊，又保持親和力。元件樣式則延續文具風格與色系，確保整體界面一致且易於使用。"
        img-url1="PlatformRedesign/designSystem1.png"
        alt1="designSystem1"
        img-url2="PlatformRedesign/designSystem2.png"
        alt2="designSystem2"
      />
    </div>
  </div>
  <ParallaxSection image="PlatformRedesign/Multiplemockups.svg" class="platform-redesign-parallax" />
  <div class="information">
    <section class="bg-info custom-padding">
      <div class="bar-target-interface position-relative">
        <div class="d-flex justify-content-center pt-16 platform-showcase-heading">
          <BaseDot text="介面展示" class="pb-4" />
        </div>
        <div class="row padding">
          <div class="col-12 col-lg-5 d-flex flex-column platform-interface-copy">
            <h4 class="fw-medium fs-7 pb-5 pt-16 w-100 platform-interface-title">
              <span class="high-light"> 清晰分層，功能定位更直覺 </span>
            </h4>
            <p class="text-start pe-24 me-24 mb-20 platform-interface-description">
              頁面以三層架構固定關鍵功能位置：第一層掌握主要操作、第二層呈現子步驟與任務、第三層聚焦表格操作。穩定的結構讓使用者不必反覆尋找，操作更高效順暢。
            </p>
          </div>
          <div class="col-12 col-lg-7 d-flex position-relative align-items-center platform-interface-visual">
            <img src="/PlatformRedesign/mockup.png" alt="interface1" class="img-position-1" />
          </div>
        </div>
      </div>
    </section>
    <section class="bg-white">
      <div>
        <div
          class="container d-flex justify-content-center align-items-center flex-column custom-padding-bottom"
        >
          <h4 class="fw-medium fs-7 pb-5 pt-16 text-center">
            <span class="high-light"> 色彩區分，資訊更清晰 </span>
          </h4>
          <p class="text-center lh-170">
            透過不同色系來代表各種資料屬性，不僅建立直觀的辨識方式，也幫助使用者快速理解資訊差異，進而避免操作上的混淆。
          </p>
          <div class="custom-width">
            <video src="/PlatformRedesign/before&after.mp4" autoplay loop muted playsinline></video>
          </div>
        </div>
      </div>
    </section>
  </div>
  <ResultSection
    content="本次專案，平台在視覺上建立了一致的設計語言，我們也期待透過分層架構、色彩區分與統一的設計系統，能讓使用者更快上手，開發與維護也更高效。在專案過程中，最大的挑戰之一是如何兼顧美觀與功能邏輯——既要確保界面漂亮、有吸引力，又要讓操作流程正確無誤。這讓我思考與嘗試了很久，也更深刻理解設計與使用者體驗之間的平衡，以及設計在提升產品效率與延展性上的關鍵角色。"
  />
  <OthersWorkSection
    img-url1="Work_Overview/CommandCenterDashboard.jpg"
    alt1="CommandCenterDashboard"
    route1="/work/commandCenterDashboard"
    img-url2="Work_Overview/LINELiff.jpg"
    alt2="LINELiff"
    route2="/work/LINELiff"
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
.custom-padding {
  padding: 60px;
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
  background-color: #cdeff5;
  opacity: 0.7;
  z-index: -1; /* 確保在文字後面 */
}

.bar-target-interface {
  overflow: hidden;
  height: 635px;
}
.img-position-1 {
  position: absolute;
  top: -3%;
  left: -4%;
  z-index: 1;
  max-width: 100%; /* 以 col-6 為基準縮放 */
}

.padding {
  padding-top: 18px;
}
.custom-width {
  width: 60%;
}
.custom-padding-bottom {
  padding-bottom: 80px;
}
.stepNumber {
  width: 36px;
  height: 36px;
}

.custom-width video {
  display: block;
  width: 100%;
  height: auto;
}

@media (max-width: 991.98px) {
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

  .platform-showcase-heading {
    padding-top: 0 !important;
  }

  .bar-target-interface > .row {
    height: auto !important;
    margin-left: 0;
    margin-right: 0;
    padding-top: 0;
  }

  .bar-target-interface > .row > .platform-interface-copy,
  .bar-target-interface > .row > .platform-interface-visual {
    width: 100%;
    max-width: 100%;
    flex: 0 0 auto;
  }

  .platform-interface-copy {
    order: 1;
    align-items: center !important;
  }

  .platform-interface-visual {
    order: 2;
    justify-content: center;
    padding-left: 0;
    padding-right: 0;
    margin-top: 32px;
  }

  .platform-interface-title {
    padding-top: 32px !important;
    padding-bottom: 20px !important;
    text-align: center;
    white-space: normal;
    font-size: 20px !important;
  }

  .platform-interface-description {
    padding: 0 !important;
    margin: 0 !important;
    text-align: center !important;
  }

  .img-position-1 {
    position: static;
    top: auto;
    left: auto;
    width: 100%;
    max-width: 100%;
    height: auto;
  }

  .custom-width {
    width: 100%;
  }

  .custom-padding-bottom {
    padding-bottom: 48px;
  }
}

@media (min-width: 768px) and (max-width: 991.98px) {
  .platform-redesign-parallax {
    height: 52vh;
    min-height: 420px;
  }

  .platform-redesign-parallax :deep(.parallax-background) {
    height: 100%;
    top: 0;
    background-size: cover;
    background-position: center center;
  }
}

@media (max-width: 390px) {
  .platform-redesign-parallax :deep(.parallax-background) {
    height: 100%;
    top: 0;
  }

  .platform-interface-title {
    font-size: 18px !important;
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
import DesignSystem from '@/components/DesignSystem.vue'
import ParallaxSection from '@/components/ParallaxSection.vue'
import ResultSection from '@/components/ResultSection.vue'
import OthersWorkSection from '@/components/OthersWorkSection.vue'

const projectTools = ['Figma', 'Illustrator']

const projectTasks = ['視覺提案', '架構規劃', 'UI Mockup']

const projectChallenges = [
  {
    title: '高資訊密度與複雜資料屬性',
    content: '平台同時呈現大量列表、圖表和多維度屬性的資料，需兼顧可讀性與篩選效率。',
  },
  {
    title: '多步驟流程的易用性設計',
    content: '試算及合約功能包含長流程表單與審核，需要簡化操作並提供清晰進度回饋，降低使用門檻。',
  },
  {
    title: '跨平台一致性與系統化設計需求',
    content:
      '多個平台早期開發時缺乏視覺統一與設計規範，造成協作與擴充困難，需要建立可延展的設計系統。',
  },
]

const targetSectionSteps = [
  {
    stepNum: '01',
    title: '降低使用門檻、提升操作效率',
    content: '透過一致性的介面設計與直覺操作流程，減少學習成本，讓使用者快速掌握大量複雜資訊。',
    img: 'PlatformRedesign/icon1.svg',
    alt: 'icon1',
  },
  {
    stepNum: '02',
    title: '靈活的資訊架構',
    content: '建立模組化與可擴充的設計系統，讓戰情資訊能隨策略變動快速更新，保持介面清晰穩定。',
    img: 'PlatformRedesign/icon2.svg',
    alt: 'icon2',
  },
  {
    stepNum: '03',
    title: '雙規格展示適配',
    content: '設計同時支援拼接螢幕與 Full HD 螢幕，讓資訊在不同展示場域都能精準傳達。',
    img: 'PlatformRedesign/icon3.svg',
    alt: 'icon3',
  },
]

const questionDefineQuestions = [
  {
    num: '1',
    title: '操作路徑不清晰',
    content: '平台資料龐大，導致使用者容易迷失在操作流程中，很難快速完成任務。',
    img: 'PlatformRedesign/problem1.png',
    alt: 'problem1',
    size: 'large',
  },
  {
    num: '2',
    title: '角色與階層模糊',
    content: '系統結構複雜，使用者難直覺的辨識自身角色與該執行的任務位置。',
    img: 'PlatformRedesign/problem2.png',
    alt: 'problem2',
  },
  {
    num: '3',
    title: '缺乏操作引導',
    content: '系統是具有明確流程邏輯，但缺少步驟之間的提示與關聯說明。',
    img: 'PlatformRedesign/problem3.png',
    alt: 'problem3',
  },
  {
    num: '4',
    title: '錯誤原因不明',
    content: '操作失敗時，系統不一定能指出缺漏或錯誤原因，增加挫折與時間成本。',
    img: 'PlatformRedesign/problem4.png',
    alt: 'problem4',
    size: 'small',
  },
]
</script>
