<script setup>
import BaseDot from '@/components/Dot.vue'
import OthersWorkSection from '@/components/OthersWorkSection.vue'
import { onMounted, onUnmounted } from 'vue'

const workExperience = [
  {
    img: 'Profile/HDRE.svg',
    company: '泓德能源科技股份有限公司',
    role: '產品設計師',
    period: '2024 三月- 目前',
    responsibilities: [
      '主要專案初期設計提案，定義視覺方向、頁面架構與 Design System，並延伸至後續功能流程、Wireframe 與 Mockup 的迭代設計。',
      '參與設計開發流程優化，從共用流程與文件建立，到導入 AI Agent 生成與實際程式碼元件一致的 Storybook，降低設計與開發間的還原落差與重複調整成本。',
    ],
  },
  {
    img: 'Profile/Beseye.svg',
    hideImage: true,
    mergeWithPrevious: true,
    company: '雲守護安控股份有限公司（後併入泓德能源）',
    role: '品牌與介面設計師',
    period: '2023 六月- 2024三月',
    responsibilities: [
      '重新規劃電動車充電操作流程，精簡使用者完成充電所需步驟，降低既有流程的操作複雜度。',
    ],
  },
  {
    img: 'Profile/WL.svg',
    company: '偉利科技股份有限公司',
    role: '設計助理',
    period: '2023 三月- 2023 五月',
    responsibilities: [
      'SEO 文章視覺素材與展覽周邊設計，累積多類型商業案件的視覺設計與執行經驗。',
    ],
  },
]
const coreSkills = [
  {
    number: '01',
    title: '介面視覺設計',
    description: '定義產品視覺方向與資訊層級',
  },
  {
    number: '02',
    title: '資訊與頁面架構',
    description: '將複雜資訊轉化為清晰的頁面結構',
  },
  {
    number: '03',
    title: '操作流程設計',
    description: '梳理功能流程並轉化為 Wireframe',
  },
  {
    number: '04',
    title: 'Design System',
    description: '建立與維護一致且可延展的介面規範',
  },
]
const designTools = [
  {
    img: 'Profile/Figma.svg',
    name: 'Figma',
  },
  {
    img: 'Profile/AI.svg',
    name: 'Illustrator',
  },
  {
    img: 'Profile/PS.svg',
    name: 'Photoshop',
  },
  {
    img: 'Profile/AE.svg',
    name: 'After Effects',
  },
]
const workflows = [
  {
    icon: 'stars',
    title: 'AI-assisted Workflow',
    description: '產出 Prototype，加速需求對焦',
  },
  {
    img: 'Profile/storybook-logo.svg',
    title: 'Storybook',
    description: 'Design-to-Code，降低設計與實作落差',
  },
]

const handleScroll = () => {
  const scrollY = window.scrollY
  const icon1 = document.querySelector('.fixed-icon-1')
  const icon2 = document.querySelector('.fixed-icon-2')

  if (icon1) {
    icon1.style.transform = `translateY(${scrollY * -0.5}px)`
  }
  if (icon2) {
    icon2.style.transform = `translateY(${scrollY * 0.4}px)` // 速度 0.4
  }
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<template>
  <!-- <div class="fixed-bg">
    <img src="/Profile/BG.png" alt="BG" />
  </div> -->
  <div class="relative background">
    <div class="fixed-icon-1">
      <img src="/Profile/BG.png" alt="icon-1" />
    </div>
    <div class="fixed-icon-2">
      <img src="/Profile/BG.png" alt="icon-2" />
    </div>
    <div class="container-xl">
      <h2 class="text-dark h1 pb-8 mb-0 fw-medium pt-8">Profile</h2>
      <div class="row custom-margin">
        <div class="col-12 col-md-4 d-flex align-items-center justify-content-center pb-4 pb-md-0">
          <img src="/Profile/photo.png" alt="Profile Photo" class="img-size" />
        </div>
        <div class="col-12 col-md-8 d-flex flex-column justify-content-center">
          <p class="lh-170 mb-2 text-custom">UI/UX Designer</p>
          <h3 class="mb-8 text-success">徐 晴 瑄</h3>
          <p class="lh-170">
            擅長透過視覺設計與頁面結構，將需求轉化為清晰且具層次的介面體驗。曾參與能源監控戰情牆、電動車充電服務、綠電媒合平台等產品，具備高資訊密度與多角色系統的介面設計經驗，能在使用需求、產品定位與開發限制間提出兼顧體驗與視覺品質的解法。
          </p>
        </div>
      </div>
    </div>
    <div class="information bg-white">
      <div class="container-xl custom-padding">
        <section class="mb-12">
          <BaseDot text="工作經歷" class="pb-8" />
          <div class="d-flex">
            <span class="side-bar"></span>
            <div class="w-100">
              <div
                v-for="(work, index) in workExperience"
                :key="index"
                class="work-entry"
                :class="{ 'work-entry--merged': work.mergeWithPrevious }"
              >
                <div class="d-md-flex">
                  <div
                    class="work-image-column pe-12 mb-4 mb-md-0"
                    :class="{ 'work-image-column--empty': work.hideImage }"
                  >
                    <div v-if="!work.hideImage" class="icon-wrap">
                      <img :src="work.img" class="icon-img" />
                    </div>
                  </div>
                  <div class="lh-170">
                    <p>{{ work.company }}</p>
                    <div class="d-flex flex-column flex-md-row">
                      <p class="border-md-end border-success pe-md-2 mb-1 mb-md-0">
                        {{ work.role }}
                      </p>
                      <p class="fw-medium ps-md-2">
                        {{ work.period }}
                      </p>
                    </div>

                    <ul>
                      <li
                        v-for="(item, idx) in work.responsibilities"
                        :key="idx"
                        class="work-description fw-normal"
                      >
                        {{ item }}
                      </li>
                    </ul>
                  </div>
                </div>

                <!-- 除了最後一筆之外才渲染分隔線 -->
                <hr
                  v-if="index < workExperience.length - 1 && !workExperience[index + 1].mergeWithPrevious"
                  class="my-8"
                />
              </div>
            </div>
          </div>
        </section>
        <section class="mb-12">
          <BaseDot text="核心專長" class="pb-8" />
          <div class="skills-grid">
            <article v-for="skill in coreSkills" :key="skill.number" class="skill-card">
              <p class="skill-number mb-2">{{ skill.number }}</p>
              <p class="skill-title mb-4">{{ skill.title }}</p>
              <p class="skill-description mb-0">{{ skill.description }}</p>
            </article>
          </div>
        </section>
        <section class="pb-8">
          <BaseDot text="工具與工作流" class="pb-4" />
          <p class="lh-170 mb-10">
            持續探索 AI 與新工具在設計流程中的應用，降低重複作業與設計開發間的落差。
          </p>
          <div class="tools-workflow-layout">
            <div class="design-tools-panel">
              <h4 class="panel-title">設計工具</h4>
              <div class="design-tools-row">
                <div v-for="tool in designTools" :key="tool.name" class="design-tool">
                  <img :src="tool.img" :alt="tool.name" />
                  <p class="mb-0">{{ tool.name }}</p>
                </div>
              </div>
            </div>
            <div class="workflow-panel">
              <h4 class="panel-title">工作流</h4>
              <div class="workflow-grid">
                <article v-for="workflow in workflows" :key="workflow.title" class="workflow-card">
                  <i v-if="workflow.icon === 'stars'" class="bi bi-stars workflow-icon" aria-hidden="true"></i>
                  <img v-else :src="workflow.img" :alt="workflow.title" class="workflow-icon" />
                  <div>
                    <p class="workflow-title mb-2 fw-semibold">{{ workflow.title }}</p>
                    <p class="workflow-description mb-0">{{ workflow.description }}</p>
                  </div>
                </article>
              </div>
            </div>
          </div>
        </section>
      </div>
    </div>
    <OthersWorkSection
      img-url1="Work_Overview/ChargingStationDSSDesign.jpg"
      alt1="ChargingStationDSSDesign"
      route1="/work/chargingStation"
      img-url2="Work_Overview/CommandCenterDashboard.jpg"
      alt2="CommandCenterDashboard"
      route2="/work/CommandCenterDashboard"
      bgClass="background"
    />
  </div>
</template>

<style scoped>
:global(html),
:global(body) {
  overflow-x: hidden;
}

.fixed-icon-1 {
  position: absolute;
  top: 0;
  right: 0;
  z-index: 0;
  pointer-events: none; /* 不影響點擊 */
  overflow: hidden;
}

.fixed-icon-1 img {
  width: 40%;
}

.fixed-icon-2 {
  position: absolute;
  bottom: 7%;
  right: 0;
  z-index: 0;
  pointer-events: none; /* 不影響點擊 */
  overflow: hidden;
}

.fixed-icon-2 img {
  width: 30%;
}
.fixed-icon-1,
.fixed-icon-2 {
  will-change: transform;
  transition: transform 0.05s linear;
}

img-size {
  width: 100%;
}

@media (max-width: 768px) {
  .img-size {
    width: 50%;
  }
}

@media (max-width: 576px) {
  .img-size {
    width: 80%;
  }
}

.custom-margin {
  margin: 40px 80px;
}

@media (max-width: 992px) {
  .custom-margin {
    margin: 32px;
  }
}

.text-custom {
  color: #8f91a2;
}

.background {
  overflow-x: hidden;
}

.information {
  width: 100%;
  position: relative;
  border-radius: 40px;
  z-index: 10;
  overflow: hidden;
}
.custom-padding {
  padding: 60px 80px;
}
@media (max-width: 768px) {
  .custom-padding {
    padding: 32px 40px;
  }
}

.side-bar {
  display: block;
  width: 7px;
  background-color: #eaf0f6;
  margin-right: 52px;
}
@media (max-width: 768px) {
  .side-bar {
    margin-right: 40px;
  }
}
.icon-wrap {
  width: 64px;
  height: 64px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.icon-img {
  max-width: 100%;
  max-height: 100%;
  object-fit: contain;
}

.work-image-column {
  flex: 0 0 116px;
}

.work-entry--merged {
  margin-top: 32px;
}

.work-description {
  color: var(--bs-secondary-color);
}

.skills-grid {
  display: grid;
  grid-template-columns: repeat(4, minmax(0, 1fr));
  gap: 24px;
}

.skill-card {
  min-height: 132px;
  padding: 20px;
  border-radius: 8px;
  background: #f1f4fa;
}

.skill-number {
  color: #d5e3f7;
  font-size: 1.25rem;
  font-weight: 500;
}

.skill-title {
  color: #77a3dd;
  font-weight: 500;
}

.skill-description,
.workflow-description {
  color: #4f505c;
  line-height: 1.7;
}

.tools-workflow-layout {
  display: grid;
  grid-template-columns: 1.1fr 1fr;
  gap: 32px;
}

.workflow-panel {
  padding-left: 32px;
  border-left: 1px solid #e1e6ef;
}

.panel-title {
  margin-bottom: 24px;
  font-size: 1rem;
  font-weight: 500;
}

.design-tools-row {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  gap: 0;
}

.design-tool {
  position: relative;
  display: flex;
  flex: 1;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  padding: 0 24px;
  text-align: center;
  color: #5b5c67;
}

.design-tool + .design-tool::before {
  position: absolute;
  top: 0;
  left: 0;
  width: 1px;
  height: 64px;
  background-color: #e1e6ef;
  content: '';
}

.design-tool img {
  width: 64px;
  height: 64px;
  margin-bottom: 16px;
  object-fit: contain;
}

.workflow-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 16px;
}

.workflow-card {
  display: flex;
  align-items: flex-start;
  gap: 16px;
  min-height: 128px;
  padding: 20px;
  border: 1px solid #d6e0f1;
  border-radius: 8px;
  background: #fbfcff;
}

.workflow-icon {
  flex: 0 0 40px;
  width: 40px;
  height: 40px;
  color: #7aa6e2;
  font-size: 2rem;
  object-fit: contain;
}

.workflow-title {
  color: #343541;
}

@media (max-width: 1100px) {
  .skills-grid {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }

  .tools-workflow-layout {
    grid-template-columns: 1fr;
  }

  .workflow-panel {
    padding-top: 32px;
    padding-left: 0;
    border-top: 1px solid #e1e6ef;
    border-left: 0;
  }
}

@media (max-width: 768px) {
  .work-image-column {
    flex-basis: auto;
    width: 100%;
  }

  .work-image-column--empty {
    display: none;
  }
}

@media (max-width: 576px) {
  .skills-grid,
  .workflow-grid {
    grid-template-columns: 1fr;
  }

  .design-tools-row {
    flex-wrap: wrap;
    justify-content: center;
    gap: 24px 0;
  }

  .design-tool {
    flex: 0 0 50%;
  }

  .design-tool:nth-child(3)::before {
    display: none;
  }

}
</style>
