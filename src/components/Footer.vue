<script setup>
defineOptions({
  name: 'AppFooter',
})
</script>

<template>
  <footer class="background border-top border-top-1 border-secondary bg-danger pb-16">
    <div class="container">
      <div class="row align-items-center justify-content-between">
        <div class="col-md-8 col-12 footer-text">
          <h4 class="lh-140 fw-normal fs-9">
            Thank You, <br />
            Let’s make something great together!
          </h4>
          <p class="text-muted lh-140">CHING DESIGN ©2025. All Rights Reserved.</p>
        </div>
        <div class="col-md-auto col-12 footer-link d-flex align-items-center">
          <a href="https://www.behance.net/chinghsuan_200028" class="pe-12">
            <div class="icon-wrapper bg-white">
              <img src="/Globe/Footer_Behance.svg" alt="behance-icon" class="icon-img" />
            </div>
          </a>
          <a href="mailto:chinghsuan2846@gmail.com">
            <div class="icon-wrapper bg-white">
              <img src="/Globe/Footer_Eenvelope.svg" alt="email-icon" class="icon-img" />
            </div>
          </a>
        </div>
      </div>
    </div>
  </footer>
</template>

<style scoped>
footer {
  padding: 70px 100px;
  position: relative;
  z-index: 2;
}
@media (max-width: 768px) {
  footer {
    padding: 24px 60px;
  }
}
@media (max-width: 390px) {
  footer {
    margin-left: 16px;
    margin-right: 16px;
  }
}
.footer-text p {
  font-size: 14px;
}
.icon-wrapper {
  width: 56px;
  height: 56px;
  border-radius: 50%;
  padding: 16px;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden; /* 保護圖片不超出邊界 */
}

.icon-img {
  width: 100%;
  height: 100%;
  object-fit: contain; /* 保證圖片比例不變 */
}
</style>
