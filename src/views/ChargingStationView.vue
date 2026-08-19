<template>
  <WorkHead
    title="智慧開電選址系統"
    content="協助業務團隊評估充電站設點的開發潛力。透過整合地理資訊、商業熱區、競爭態勢與電力可行性等多維度資料，系統可自動計算場址評分，提供具體化選址建議，提升開發效率與成功率。"
    tag="Charging Station DSS Design"
    img-url="ChargingStation/titleImg.png"
    alt="titleImg"
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
        img-url="ChargingStation/projectChallenge.png"
        alt="專案挑戰圖"
      />
      <hr class="my-12" />
      <TargetSection :steps="targetSectionSteps" />
      <hr class="my-12" />
      <section>
        <BaseDot text="選址流程" class="pb-4" />
        <p class="pb-12">
          觀察業務選址流程後，發現資料分散且操作繁複。因此將設計重點放在資料整合、可視化呈現與圖層篩選功能，提升使用效率與決策便利性。
        </p>

        <div class="d-flex flex-column flex-lg-row justify-content-between align-items-center g-0">
          <div class="col-12 col-lg-3">
            <div class="card bg-warning border-1 border-light">
              <div class="card-body p-8">
                <div class="d-flex flex-column align-items-center">
                  <p class="bg-success text-white custom-rounded fw-medium mb-0">
                    <span class="fs-8">01</span> 收集場址
                  </p>
                  <img src="/ChargingStation/address1.svg" alt="address1" class="my-8" />
                  <p class="card-text text-center">
                    透過投標或地主提供的資料，整理出可能的候選地點
                  </p>
                </div>
              </div>
            </div>
          </div>

          <div class="col-12 col-lg-1 d-flex justify-content-center py-4 py-lg-0">
            <img src="/LINELiff/Arrow.svg" alt="箭頭" class="rotate-mobile" />
          </div>

          <div class="col-12 col-lg-3">
            <div class="card bg-warning border-1 border-light">
              <div class="card-body p-8">
                <div class="d-flex flex-column align-items-center">
                  <p class="bg-success text-white custom-rounded fw-medium mb-0">
                    <span class="fs-8">02</span> 多平台查詢
                  </p>
                  <img src="/ChargingStation/address2.svg" alt="address2" class="my-8" />
                  <p class="card-text text-center">
                    透過 Excel、Google Map 與其他報表平台，分別查看數據。
                  </p>
                </div>
              </div>
            </div>
          </div>

          <div class="col-12 col-lg-1 d-flex justify-content-center py-4 py-lg-0">
            <img src="/LINELiff/Arrow.svg" alt="箭頭" class="rotate-mobile" />
          </div>

          <div class="col-12 col-lg-3">
            <div class="card bg-warning border-1 border-light">
              <div class="card-body p-8">
                <div class="d-flex flex-column align-items-center">
                  <p class="bg-success text-white custom-rounded fw-medium mb-0">
                    <span class="fs-8">03</span> 整合與決策
                  </p>
                  <img src="/ChargingStation/address3.svg" alt="address3" class="my-8" />
                  <p class="card-text text-center">將不同來源數據輸入 Excel 並進行場址評估。</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
      <hr class="my-12" />
      <QuestionSection
        content="透過使用流程的分析，我們發現部分操作不夠直覺，功能安排也沒完全符合使用者在充電時的實際需求，這成為後續優化的重點。"
        :questions="questionDefineQuestions"
      />
      <hr class="my-12" />
      <section>
        <BaseDot text="需求與功能優先級分類" class="pb-4" />
        <p class="pb-4">初步規劃系統的三大功能基礎，為後續設計提供方向。</p>
        <div class="row g-4 mb-12">
          <div class="col-12 col-md-4 d-flex">
            <div class="card bg-warning border-1 w-100">
              <div
                class="card-body p-8 d-flex flex-row flex-md-column flex-lg-row align-items-center w-100"
              >
                <div
                  class="d-flex align-items-center flex-shrink-0 border-end border-md-bottom border-lg-end border-secondary pe-4 me-4 pe-md-0 me-md-0 pe-lg-4 me-lg-4 pb-0 mb-0 pb-md-3 mb-md-3 pb-lg-0 mb-lg-0"
                >
                  <span
                    class="stepNumber fw-bold d-inline-flex justify-content-center align-items-center rounded-circle bg-success text-white lh-170 flex-shrink-0"
                  >
                    01
                  </span>
                  <h4 class="fw-medium lh-170 text-success fs-9 mb-0 ms-3 text-nowrap">場址輸入</h4>
                </div>

                <div class="flex-grow-1">
                  <p class="mb-0 text-start text-md-center text-lg-start">收集整理場址相關資訊</p>
                </div>
              </div>
            </div>
          </div>

          <div class="col-12 col-md-4 d-flex">
            <div class="card bg-warning border-1 w-100">
              <div
                class="card-body p-8 d-flex flex-row flex-md-column flex-lg-row align-items-center w-100"
              >
                <div
                  class="d-flex align-items-center flex-shrink-0 border-end border-md-bottom border-lg-end border-secondary pe-4 me-4 pe-md-0 me-md-0 pe-lg-4 me-lg-4 pb-0 mb-0 pb-md-3 mb-md-3 pb-lg-0 mb-lg-0"
                >
                  <span
                    class="stepNumber fw-bold d-inline-flex justify-content-center align-items-center rounded-circle bg-success text-white lh-170 flex-shrink-0"
                    >02</span
                  >
                  <h4 class="fw-medium lh-170 text-success fs-9 mb-0 ms-3 text-nowrap">潛力評估</h4>
                </div>
                <div class="flex-grow-1">
                  <p class="mb-0 text-start text-md-center text-lg-start">瀏覽分析各場址的優劣</p>
                </div>
              </div>
            </div>
          </div>

          <div class="col-12 col-md-4 d-flex">
            <div class="card bg-warning border-1 w-100">
              <div
                class="card-body p-8 d-flex flex-row flex-md-column flex-lg-row align-items-center w-100"
              >
                <div
                  class="d-flex align-items-center flex-shrink-0 border-end border-md-bottom border-lg-end border-secondary pe-4 me-4 pe-md-0 me-md-0 pe-lg-4 me-lg-4 pb-0 mb-0 pb-md-3 mb-md-3 pb-lg-0 mb-lg-0"
                >
                  <span
                    class="stepNumber fw-bold d-inline-flex justify-content-center align-items-center rounded-circle bg-success text-white lh-170 flex-shrink-0"
                    >03</span
                  >
                  <h4 class="fw-medium lh-170 text-success fs-9 mb-0 ms-3 text-nowrap">決策支援</h4>
                </div>
                <div class="flex-grow-1">
                  <p class="mb-0 text-start text-md-center text-lg-start">生成評級支援選址判斷</p>
                </div>
              </div>
            </div>
          </div>
        </div>
        <p class="pb-4">
          在三大功能基礎上，依據業務需求展開各項功能，並進行優先排序與分類，確保設計與開發聚焦核心價值。
        </p>
        <div class="row">
          <div class="col-12 col-lg-4">
            <h4 class="fw-medium lh-170 fs-9 text-success pb-4 d-flex">
              <img src="/ChargingStation/MustHavePin.svg" alt="MustHavePin" class="pe-2" />Must Have
            </h4>
            <table class="table table-rounded">
              <thead>
                <tr class="table-info">
                  <th scope="col" width="40%">功能</th>
                  <th scope="col" width="60%">描述</th>
                </tr>
              </thead>
              <tbody>
                <tr>
                  <th scope="row">地址搜尋</th>
                  <td>串聯 Google 地圖，快速搜尋定位場址</td>
                </tr>
                <tr>
                  <th scope="row">可視化數據</th>
                  <td>熱力圖與互動地圖，直觀呈現多維數據</td>
                </tr>
                <tr>
                  <th scope="row">圖層篩選</th>
                  <td>篩選切換家戶、車流、景點與競爭分布圖層</td>
                </tr>
                <tr>
                  <th scope="row">評分系統</th>
                  <td>多維度分析產出評分，減少人工比對</td>
                </tr>
                <tr>
                  <th scope="row">年度度數預估</th>
                  <td>預測年度充電度數，降低錯誤決策風險</td>
                </tr>
              </tbody>
            </table>
          </div>
          <div class="col-12 col-lg-4">
            <h4 class="fw-medium lh-170 fs-9 text-success pb-4 d-flex">
              <img
                src="/ChargingStation/NicetoHaveStar.svg"
                alt="NicetoHaveStar"
                class="pe-2"
              />Nice to Have
            </h4>
            <table class="table table-rounded">
              <thead>
                <tr class="table-info">
                  <th scope="col" width="40%">功能</th>
                  <th scope="col" width="60%">描述</th>
                </tr>
              </thead>
              <tbody>
                <tr>
                  <th scope="row">多站點匯入</th>
                  <td>一次上傳多地址，自動分析並給出評分</td>
                </tr>
                <tr>
                  <th scope="row">報表匯出</th>
                  <td>評分結果可匯出，方便彙整決策應用</td>
                </tr>
                <tr>
                  <th scope="row">歷史紀錄</th>
                  <td>保存過往站點數據，方便比較與規劃</td>
                </tr>
              </tbody>
            </table>
          </div>
          <div class="col-12 col-lg-4">
            <h4 class="fw-medium lh-170 fs-9 text-success pb-4 d-flex">
              <img
                src="/ChargingStation/CanComeLaterLamp.svg"
                alt="CanComeLaterLamp"
                class="pe-2"
              />Can Come Later
            </h4>
            <table class="table table-rounded">
              <thead>
                <tr class="table-info">
                  <th scope="col" width="40%">功能</th>
                  <th scope="col" width="60%">描述</th>
                </tr>
              </thead>
              <tbody>
                <tr>
                  <th scope="row">AI 推薦</th>
                  <td>系統透過 AI，自動推薦最佳候選站點</td>
                </tr>
                <tr>
                  <th scope="row">Google 街景</th>
                  <td>即時預覽站點周邊街景，確認環境條件</td>
                </tr>
              </tbody>
            </table>
          </div>
        </div>
      </section>
      <hr class="my-12" />
      <InformationArchitecture
        content="根據前階段對任務流程的梳理與問題定義，我們重新規劃了頁面結構與功能配置。"
        img-url="ChargingStation/informationArchitecture.svg"
        alt="informationArchitectureImg"
      />
      <hr class="my-12" />
      <DesignSystem
        content="系統採用深色背景，搭配品牌藍綠作為核心元素，營造一致且專業的視覺風格。"
        img-url1="ChargingStation/designSystem1.png"
        alt1="designSystem1"
        img-url2="ChargingStation/designSystem2.png"
        alt2="designSystem2"
      />
    </div>
  </div>
  <ParallaxSection image="ChargingStation/mockup.svg" class="charging-station-parallax" />
  <div class="information">
    <section class="bg-white custom-padding">
      <div class="container">
        <BaseDot text="易用性測試" class="pb-12" />
        <div class="usability-task mb-12">
          <p class="usability-task-badge bg-success text-white custom-rounded-2 fw-bold mb-0 fs-8 lh-140">
            站點評估
          </p>
          <ul class="usability-task-list lh-170 ps-8">
            <li>任務情境：業務取得地址，需要透過系統進行建站評估，生成評分</li>
            <li>任務目的：了解使用者能否透過系統快速評估建站潛力，與操作準確性</li>
          </ul>
        </div>
        <h4 class="fw-medium fs-7 pb-4">Before</h4>
        <img
          src="/ChargingStation/Usability_before.png"
          alt="Usability_before"
          class="img-fluid w-100 mb-12"
        />
        <img src="/ChargingStation/feedback.png" alt="feedback" class="img-fluid w-100 mb-12" />
        <h4 class="fw-medium fs-7 pb-4">After</h4>
        <img
          src="/ChargingStation/Usability_After.png"
          alt="Usability_After"
          class="img-fluid w-100"
        />
      </div>
    </section>
    <section class="bg-info">
      <div>
        <div class="bar-target-interface interface-showcase-first position-relative">
          <div class="bar-line" style="top: 272px">
            <div class="bar-line-body-left"></div>
          </div>
          <div class="d-flex justify-content-center pt-16 interface-showcase-heading">
            <BaseDot text="介面展示" class="pb-4" />
          </div>
          <div class="row h-100">
            <div class="col-12 col-lg-6 d-flex position-relative interface-visual">
              <img src="/ChargingStation/interface1.png" alt="interface1" class="img-position-1" />
            </div>
            <div class="col-12 col-lg-5 d-flex flex-column align-items-end interface-copy">
              <h4 class="fw-medium fs-7 pb-5 custom-padding-1 interface-title">
                <span class="high-light"> 熱力圖色彩規劃 </span>
              </h4>
              <p class="interface-description text-end pt-8 ps-24 ms-24 mb-20">
                為保持深色背景的設計感，同時避免紅色帶來警示感，熱力圖採用藍綠漸變，密集區域以淺亮色呈現，兼顧直覺性與視覺美感
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="bg-white">
      <div>
        <div class="bar-target-interface position-relative">
          <div class="bar-line" style="top: 279px">
            <div class="bar-dot-right"></div>
            <div class="bar-line-body-right"></div>
          </div>
          <div class="row justify-content-between h-100">
            <div class="offset-0 offset-lg-1 col-12 col-lg-5 d-flex flex-column align-items-start interface-copy">
              <h4 class="fw-medium fs-7 pb-5 custom-padding-2 interface-title">
                <span class="high-light"> 可視化地圖，一眼掌握最佳分布！ </span>
              </h4>
              <p class="interface-description text-start pt-8 pe-20 me-20 mb-20">
                系統以直觀地圖呈現場址與周邊資訊，從行政區到村里不同粒度的資料都能清楚展示，幫助使用者快速掌握最佳分布與潛在熱區。
              </p>
            </div>
            <div class="col-12 col-lg-6 d-flex align-items-center position-relative interface-visual">
              <img src="/ChargingStation/interface2.png" alt="interface2" class="img-position-2" />
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="bg-info">
      <div>
        <div class="bar-target-interface position-relative">
          <div class="bar-line" style="top: 274px">
            <div class="bar-dot-left-2"></div>
            <div class="bar-line-body-left-2"></div>
          </div>
          <div class="row h-100">
            <div class="col-12 col-lg-6 d-flex align-items-center position-relative interface-visual">
              <img src="/ChargingStation/interface3.png" alt="interface3" class="img-position-3" />
            </div>
            <div class="col-12 col-lg-5 d-flex flex-column align-items-end interface-copy">
              <h4 class="fw-medium fs-7 pb-5 custom-padding-3 interface-title">
                <span class="high-light"> 多維度數據整合，靈活圖層篩選！ </span>
              </h4>
              <p class="interface-description text-end pt-8 ps-24 ms-24 mb-20">
                整合交通流量、家戶數、POI
                景點、競爭品牌等多種資料，並提供靈活圖層切換功能，讓使用者依需求查看不同資訊維度，提升分析效率。
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="bg-white">
      <div>
        <div class="bar-target-interface position-relative">
          <div class="bar-line" style="top: 279px">
            <div class="bar-line-body-right-2"></div>
          </div>
          <div class="row justify-content-between h-100">
            <div class="offset-0 offset-lg-1 col-12 col-lg-5 d-flex flex-column align-items-start interface-copy">
              <h4 class="fw-medium fs-7 pb-5 custom-padding-4 interface-title">
                <span class="high-light"> 智能選址評分，助你精準決策！ </span>
              </h4>
              <p class="interface-description text-start pt-8 pe-24 me-24 mb-20">
                自動對輸入的場址進行評分，結合多項指標提供量化參考，協助業務精準判斷每個場址的開發潛力與優先順序。
              </p>
            </div>
            <div class="col-12 col-lg-6 d-flex align-items-center position-relative interface-visual">
              <img src="/ChargingStation/interface4.png" alt="interface4" class="img-position-4" />
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
  <ResultSection
    content="透過本專案，我將複雜的數據分析流程轉化為直觀的介面體驗，幫助業務在更短時間內完成選址評估。雖然過程中面臨資料顯示限制與色彩規劃挑戰，但最終透過合理的資訊分層與品牌化設計，成功打造出一套兼具專業與易用性的決策輔助工具。這次經驗也讓我更深刻理解如何在數據密集的情境下，透過 UI/UX 設計提升資訊可讀性與決策效率。"
  />
  <OthersWorkSection
    img-url1="Work_Overview/LINELiff.jpg"
    alt1="LINELiff"
    route1="/work/LINELiff"
    img-url2="Work_Overview/CommandCenterDashboard.jpg"
    alt2="CommandCenterDashboard"
    route2="/work/commandCenterDashboard"
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
.usability-task::after {
  content: '';
  display: block;
  clear: both;
}
.usability-task-badge {
  float: left;
  white-space: nowrap;
  margin-right: 40px !important;
}
.usability-task-list {
  margin-bottom: 0;
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
  background-color: #b0f5e6;
  opacity: 0.7;
  z-index: -1; /* 確保在文字後面 */
}
.custom-padding-1 {
  padding-top: 124px;
}
.custom-padding-2 {
  padding-top: 225px;
}
.custom-padding-3 {
  padding-top: 220px;
}
.custom-padding-4 {
  padding-top: 225px;
}
.custom-padding-5 {
  padding: 100px 176px;
}
.bar-target-interface {
  overflow: hidden;
  height: 600px;
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
.bar-line-body-left {
  position: absolute;
  left: 42%;
  width: 50%;
  height: 1px;
  background-color: #769bd9;
  top: 2.5px;
}
.bar-dot-right {
  position: absolute;
  right: 46.5%;
  width: 6px;
  height: 6px;
  background-color: #769bd9;
  border-radius: 50%;
  transform: translateX(50%);
  top: 0;
}
.bar-line-body-right {
  position: absolute;
  right: 46.5%;
  width: 45.5%;
  height: 1px;
  background-color: #769bd9;
  top: 2.5px;
}
.bar-dot-left-2 {
  position: absolute;
  left: 37.7%;
  width: 6px;
  height: 6px;
  background-color: #769bd9;
  border-radius: 50%;
  transform: translateX(-50%);
  top: 0;
}
.bar-line-body-left-2 {
  position: absolute;
  left: 37.7%;
  width: 54%;
  height: 1px;
  background-color: #769bd9;
  top: 2.5px;
}
.bar-line-body-right-2 {
  position: absolute;
  right: 36.75%;
  width: 55%;
  height: 1px;
  background-color: #769bd9;
  top: 2.5px;
}
.img-position-1 {
  position: absolute;
  left: -6%;
  z-index: 1;
  max-width: 100%; /* 以 col-6 為基準縮放 */
}
.img-position-2 {
  max-width: 100%; /* 以 col-6 為基準縮放 */
}
.img-position-3 {
  position: absolute;
  left: -21%;
  z-index: 1;
  max-width: 100%; /* 以 col-6 為基準縮放 */
}
.img-position-4 {
  width: 90%;
  position: absolute;
  right: -14%;
  z-index: 1;
}
.stepNumber {
  width: 36px;
  height: 36px;
}

.rotate-mobile {
  transform: rotate(90deg);
}

@media (min-width: 992px) {
  .rotate-mobile {
    transform: rotate(0deg);
  }
}
@media (min-width: 768px) and (max-width: 991.98px) {
  .border-md-bottom {
    border-right: 0 !important;
    border-bottom: 1px solid #b8cade !important;
    width: 100%;
    justify-content: center;
  }
}

/* 2. 當處於手機或電腦時，確保只有右邊框 */
@media (max-width: 767.98px), (min-width: 992px) {
  .border-end,
  .border-lg-end {
    border-right: 1px solid #b8cade !important;
    border-bottom: 0 !important;
  }
}

@media (max-width: 991.98px) {
  /* Keep the same page gutter as the LINE Liff case study. */
  .information > .container-xl.custom-padding {
    padding: 60px 24px;
  }

  .information > section.custom-padding,
  .information > section:not(.custom-padding) {
    padding-left: 24px;
    padding-right: 24px;
  }

  .bar-target-interface {
    height: auto;
    min-height: 0;
    padding: 48px 0 64px;
  }

  .interface-showcase-first {
    padding-top: 32px;
  }

  .interface-showcase-first .interface-showcase-heading {
    padding-top: 48px !important;
  }

  .bar-target-interface > .row {
    height: auto !important;
    margin-left: 0;
    margin-right: 0;
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
    width: 100%;
    padding-top: 32px !important;
    padding-bottom: 20px !important;
    text-align: center;
    white-space: normal;
    font-size: 20px !important;
  }

  .interface-description {
    padding: 0 !important;
    margin: 0 0 32px !important;
    text-align: center !important;
  }

  .interface-visual .img-position-1,
  .interface-visual .img-position-2,
  .interface-visual .img-position-3,
  .interface-visual .img-position-4 {
    position: static;
    left: auto;
    right: auto;
    width: 100%;
    max-width: 100%;
    height: auto;
    transform: none;
  }

  .interface-visual .img-position-1,
  .interface-visual .img-position-4 {
    width: 90%;
  }

  .custom-padding-1,
  .custom-padding-2,
  .custom-padding-3,
  .custom-padding-4 {
    padding-top: 32px;
  }
}

@media (max-width: 991.98px) {
  .usability-task {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
  }

  .usability-task::after {
    display: none;
  }

  .usability-task-badge {
    float: none;
    margin-right: 0 !important;
    margin-bottom: 24px !important;
  }

  .usability-task-list {
    width: 100%;
    padding-left: 24px !important;
  }
}

@media (min-width: 768px) and (max-width: 991.98px) {
  .interface-title {
    white-space: nowrap;
  }
}

@media (max-width: 390px) {
  .charging-station-parallax :deep(.parallax-background) {
    height: 120%;
    top: -10%;
  }

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

const projectTools = ['Figma', 'Illustrator']

const projectTasks = ['Task Flow', '設計系統', 'UI Mockup', 'UI Hand-off']

const projectChallenges = [
  {
    title: '多維度資料的可視化呈現',
    content:
      '需將家戶數、車輛數、車流量、POI 與競爭品牌等多種來源的數據整合於同一地圖，並透過色彩與圖層設計，讓業務能快速理解而不被資訊淹沒。',
  },
  {
    title: '地圖縮放層級的資訊分層設計',
    content:
      '地圖需根據縮放層級依序呈現縣市、鄉鎮市區、村里等不同粒度的統計與評分資料。必須明確定義各層級的顯示內容，確保使用者在不同視圖下獲得最適合的資訊。',
  },
  {
    title: '傳統工具流程轉換的操作體驗設計',
    content:
      '業務原以 Excel 與 Google Map 交叉比對場址，流程繁瑣且易出錯。系統需整合資料與地圖於單一介面，簡化操作並提升效率。',
  },
]

const targetSectionSteps = [
  {
    stepNum: '01',
    title: '清晰資訊架構',
    content:
      '設計直觀的圖層與視覺化元素，有效整合多元資料，讓使用者能迅速抓住關鍵資訊，避免資訊過載。',
    img: 'ChargingStation/designTarget1.svg',
    alt: 'designTarget1',
  },
  {
    stepNum: '02',
    title: '動態資料呈現策略',
    content: '根據地圖縮放層級，精準定義與切換不同粒度資料，確保資訊在各層級皆清晰且易於理解。',
    img: 'ChargingStation/designTarget2.svg',
    alt: 'designTarget2',
  },
  {
    stepNum: '03',
    title: '流程簡化與整合',
    content:
      '將多重資料與地圖功能整合於單一介面，統一資料來源。簡化操作流程，節省評估時間並提升選址精準度。',
    img: 'ChargingStation/designTarget3.svg',
    alt: 'designTarget3',
  },
]

const questionDefineQuestions = [
  {
    num: '1',
    title: '資料來源分散，整合繁瑣',
    content: '數據分散在多個平台，手動整合耗時且容易出錯',
    img: 'ChargingStation/questionDefine1.svg',
    alt: 'questionDefine1',
  },
  {
    num: '2',
    title: '缺乏高效的數據比對工具',
    content: '缺少自動比對機制，場址評估效率低，操作繁瑣',
    img: 'ChargingStation/questionDefine2.svg',
    alt: 'questionDefine2',
  },
  {
    num: '3',
    title: '需求預測準確度不足',
    content: '依賴人工整合與經驗判斷，數據分散或缺漏容易導致預測不準',
    img: 'ChargingStation/questionDefine3.svg',
    alt: 'questionDefine3',
  },
  {
    num: '4',
    title: '缺乏即時更新的資料',
    content: '資料更新慢，決策依賴手動更新資訊，降低效率',
    img: 'ChargingStation/questionDefine4.svg',
    alt: 'questionDefine4',
  },
]
</script>
