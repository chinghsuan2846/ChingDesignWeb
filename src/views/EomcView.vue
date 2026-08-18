<template>
  <WorkHead
    title="企業營運中心管理系統"
    content="整合公司各事業單位的營運與財務數據，提供主管快速掌握整體營運狀況與關鍵指標。各單位可透過管理後台維護與上傳資料，並將資訊整合至決策中心，作為營運檢視、會議報告與決策判斷的依據。"
    tag="Dashboard"
    img-url="EOMC/overview.jpg"
    alt="企業營運中心管理系統介面"
  />

  <div class="information bg-white">
    <div class="container-xl custom-padding">
      <ProjectInformation
        role="UI/UX 設計師"
        project-duration="前期設計 1 個月，持續迭代中"
        duration-label="專案週期"
        :tools="projectTools"
        :tasks="projectTasks"
      />

      <hr class="my-12" />

      <ProjectChallenge
        :challenges="projectChallenges"
        img-url="EOMC/challenge.jpg"
        alt="營運資料圖表"
      />

      <hr class="my-12" />

      <TargetSection :steps="targetSectionSteps" />

      <hr class="my-12" />

      <section>
        <BaseDot text="設計系統" class="pb-4" />
        <p class="section-copy pb-12 mb-0">
          建立一致且可延展的介面規則，透過語意色彩與資料卡片模式，提升資訊判讀效率，並支援不同營運資訊的彈性呈現。
        </p>
        <div class="row gx-12 gy-8">
          <div class="col-12 col-md-6">
            <img src="/EOMC/designsystem-semanticcolor.png" alt="語意色彩設計系統" class="content-image" />
          </div>
          <div class="col-12 col-md-6">
            <img src="/EOMC/designsystem-cardpatterns.png" alt="資料卡片設計模式" class="content-image" />
          </div>
        </div>
      </section>

      <hr class="my-12" />

      <section class="storybook-section">
        <BaseDot text="Storybook" class="pb-4" />
        <p class="section-copy mb-8">
          透過 AI Agent 與 Storybook 建立接近實際產品的元件環境，讓設計確認提前發生，降低設計與開發間的還原落差。
        </p>
        <div class="flow-label">Before</div>
        <div class="flow-row before-flow mb-6">
          <div>Figma<br />Handoff</div>
          <span>→</span>
          <div>Development</div>
          <span>→</span>
          <div>Design QA</div>
          <span>→</span>
          <div>Revision</div>
        </div>
        <div class="flow-label">After</div>
        <div class="flow-row after-flow mb-8">
          <div>AI + Skills<br />產生元件</div>
          <span>→</span>
          <div>Storybook<br />實際元件環境</div>
          <span>→</span>
          <div>設計師自行<br />調整畫面</div>
        </div>
        <img src="/EOMC/storybook.png" alt="Storybook 元件展示" class="content-image storybook-image" />
      </section>
    </div>
  </div>

  <ParallaxSection image="EOMC/Multiple mockups.png" class="eomc-parallax" />

  <section class="interface-showcase bg-white">
    <div class="container-xl showcase-inner">
      <BaseDot text="介面展示" class="justify-content-center pb-4" />
      <h3 class="text-center fw-medium mb-4">彈性組合資訊模組，因應多變的營運需求</h3>
      <p class="section-copy text-center showcase-copy">
        依據資訊量與閱讀優先級配置不同尺寸的卡片模組，讓頁面能隨內容需求彈性調整，同時維持一致的資訊層級與閱讀體驗。
      </p>
      <img src="/EOMC/ui-bento.png" alt="彈性組合資訊模組" class="content-image bento-image" />
    </div>

    <div class="showcase-split bg-info">
      <div class="container-xl row align-items-center g-12">
        <div class="col-12 col-lg-6 showcase-media">
          <img src="/EOMC/ui-semanticcolor.png" alt="語意色彩介面" class="content-image" />
        </div>
        <div class="col-12 col-lg-6 showcase-copy-block">
          <h3 class="fw-medium">以色彩區分資訊狀態，讓異常一眼可見</h3>
          <p class="section-copy">
            透過綠色與橘色區分正常與異常資訊，降低數據判讀負擔，協助使用者快速聚焦需要關注的數值。
          </p>
        </div>
      </div>
    </div>

    <div class="showcase-split">
      <div class="container-xl row align-items-center g-12">
        <div class="col-12 col-lg-6 showcase-copy-block">
          <h3 class="fw-medium">延續一致操作邏輯，降低功能擴充的學習成本</h3>
          <p class="section-copy">
            將常見管理任務整理為一致的操作模式，讓不同功能沿用相同的搜尋、檢視與編輯邏輯，使系統持續擴充時仍能維持熟悉的使用體驗。
          </p>
        </div>
        <div class="col-12 col-lg-6 showcase-media">
          <img src="/EOMC/ui-backplatform.png" alt="後台管理介面" class="content-image" />
        </div>
      </div>
    </div>
  </section>

  <ResultSection
    content="這次專案讓我體會到，面對持續變動的營運需求，比起設計一套固定的最佳版型，建立能承接變化的介面規則更重要。同時透過 Storybook 與 AI 輔助工作流，嘗試縮短設計與實際產品間的落差，也讓設計能更早在接近真實開發的環境中被確認與調整。"
  />

  <OthersWorkSection
    img-url1="Work_Overview/CommandCenterDashboard.jpg"
    alt1="能源戰情系統展示牆"
    route1="/work/commandCenterDashboard"
    img-url2="Work_Overview/PlatformRedesign.jpg"
    alt2="綠電平台視覺與架構優化"
    route2="/work/platformRedesign"
  />
</template>

<script setup>
import BaseDot from '@/components/Dot.vue'
import WorkHead from '@/components/WorkHead.vue'
import ProjectInformation from '@/components/ProjectInformation.vue'
import ProjectChallenge from '@/components/ProjectChallenge.vue'
import TargetSection from '@/components/TargetSection.vue'
import ParallaxSection from '@/components/ParallaxSection.vue'
import ResultSection from '@/components/ResultSection.vue'
import OthersWorkSection from '@/components/OthersWorkSection.vue'

const projectTools = ['Figma', 'AI + Storybook']

const projectTasks = ['視覺提案', 'Design System', 'Wireframe', 'UI Hand-off']

const projectChallenges = [
  {
    title: '多來源資訊整合',
    content: '各事業單位的營運與財務資料類型不一，需要建立清楚的資訊層級，協助主管快速掌握關鍵資訊。',
  },
  {
    title: '動態變化的資訊需求',
    content: '營運指標與呈現需求會隨管理情境持續調整，介面需具備足夠彈性，因應資訊內容與數量的變化。',
  },
  {
    title: '特殊尺寸適配',
    content: '後台功能會隨需求持續擴充，因此需建立一致的操作模式，降低新增功能帶來的學習成本。',
  },
]

const targetSectionSteps = [
  {
    stepNum: '01',
    title: '快速掌握關鍵資訊',
    content: '透過資訊層級與狀態設計，突出關鍵指標、趨勢與異常資訊，協助使用者快速掌握營運狀況。',
    img: 'EOMC/專案目標-viewfinder-circle.svg',
    alt: '快速掌握關鍵資訊',
  },
  {
    stepNum: '02',
    title: '建立彈性的資訊架構',
    content: '以模組化架構承載不同類型資訊，因應指標、內容與數量變化，保留後續擴充與調整的彈性。',
    img: 'EOMC/專案目標-squares-plus.svg',
    alt: '建立彈性的資訊架構',
  },
  {
    stepNum: '03',
    title: '維持一致的操作邏輯',
    content: '建立共用的元件與操作模式，讓後台功能持續擴充時，仍能維持一致且易理解的使用體驗。',
    img: 'EOMC/專案目標-cog-8-tooth.svg',
    alt: '維持一致的操作邏輯',
  },
]
</script>

<style scoped>
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

.section-copy {
  line-height: 170%;
  color: #25262d;
}

.information :deep(.img-padding) {
  width: calc(100% - 80px);
  margin-left: 80px;
  padding-left: 0;
  border-radius: 12px;
}

.content-image {
  width: 100%;
  height: auto;
  border-radius: 12px;
}

.storybook-image {
  border: 1px solid #e5eaf3;
  height: 420px;
  object-fit: cover;
  object-position: top;
}

.flow-label {
  color: #769bd9;
  margin-bottom: 8px;
}

.flow-row {
  display: flex;
  align-items: center;
  gap: 16px;
}

.flow-row div {
  flex: 1;
  min-height: 58px;
  border: 1px solid #d7e0f0;
  border-radius: 4px;
  background-color: #f9f9fd;
  color: #25262d;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  line-height: 150%;
  padding: 8px;
}

.flow-row span {
  color: #769bd9;
  font-size: 24px;
}

.after-flow div {
  background-color: #f0f3f9;
  color: #769bd9;
}

.interface-showcase {
  position: relative;
  z-index: 10;
  overflow: hidden;
}

.showcase-inner {
  padding: 100px 60px 120px;
}

.showcase-inner h3 {
  font-size: 1.5rem;
}

.showcase-copy {
  max-width: 720px;
  margin: 0 auto 48px;
}

.bento-image {
  display: block;
  max-width: 88%;
  margin: 0 auto;
  border-radius: 18px;
}

.showcase-split {
  padding: 110px 60px;
}

.showcase-split .container-xl {
  max-width: 1320px;
  margin: 0 auto;
}

.showcase-split h3 {
  font-size: 1.5rem;
  line-height: 150%;
  margin-bottom: 24px;
}

@media (max-width: 991.98px) {
  .information {
    border-radius: 24px;
  }

  .information > .container-xl.custom-padding {
    padding: 60px 24px;
  }

  .information :deep(.img-padding) {
    width: calc(100% - 40px);
    margin-left: 40px;
  }

  .flow-row {
    gap: 6px;
  }

  .flow-row span {
    font-size: 18px;
  }

  .flow-row div {
    font-size: 12px;
    min-height: 64px;
  }

  .storybook-image {
    height: auto;
    object-fit: contain;
  }

  .showcase-inner,
  .showcase-split {
    padding: 64px 24px;
  }

  .showcase-inner h3 {
    font-size: 20px;
  }

  .showcase-split h3 {
    font-size: 20px;
  }

  .bento-image {
    width: 100%;
    max-width: 100%;
  }

  .showcase-copy {
    margin-bottom: 32px;
  }

  .showcase-split .container-xl.row {
    width: 100%;
    max-width: none;
    margin-left: 0;
    margin-right: 0;
    --bs-gutter-x: 0;
    --bs-gutter-y: 0;
  }

  .showcase-split .container-xl.row > [class*='col-'] {
    padding-left: 0;
    padding-right: 0;
  }

  .showcase-split .container-xl.row > [class*='col-'] + [class*='col-'] {
    margin-top: 0;
  }

  .showcase-split .showcase-copy-block {
    order: 1;
    text-align: center;
  }

  .showcase-split .showcase-media {
    order: 2;
    margin-top: 32px !important;
  }
}

@media (max-width: 390px) {
  .eomc-parallax :deep(.parallax-background) {
    height: 100%;
    top: 0;
  }

  .showcase-inner,
  .showcase-split {
    padding: 48px 24px 56px;
  }

  .showcase-inner h3,
  .showcase-split h3 {
    font-size: 18px;
  }

  .showcase-copy,
  .showcase-split .section-copy {
    font-size: 14px;
  }

  .showcase-copy {
    margin-bottom: 24px;
  }

  .flow-row {
    gap: 4px;
  }

  .flow-row div {
    font-size: 11px;
    min-height: 60px;
    padding: 6px 4px;
  }

  .flow-row span {
    font-size: 16px;
  }
}
</style>
