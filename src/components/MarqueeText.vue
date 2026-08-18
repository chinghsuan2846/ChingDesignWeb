<template>
  <div class="marquee w-100">
    <div class="marquee-bg"></div>
    <div class="fs-5 fw-medium d-flex align-items-center special-text">
      <span>{{ props.content }}</span>
      <span>{{ props.content }}</span>
      <span>{{ props.content }}</span>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  content: {
    type: String,
    required: true,
  },
})
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Saira:wght@400;500;600;700&display=swap');

.marquee {
  height: 64px;
  position: relative;
  background: #111; /* 外框底色，可自行調整 */
  overflow: hidden;
}

/* 背景固定，不跟動畫一起動 */
.marquee-bg {
  position: absolute;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, #4185af, #37be84);
}

/* 文字區塊跑馬動畫 */
.marquee div:not(.marquee-bg) {
  display: block;
  width: 200%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
  overflow: hidden;
  background: none; /* 移除背景，避免跟動畫一起動 */
  animation: marquee 8s linear infinite;
  line-height: 1;
}

.marquee span {
  float: left;
  width: 50%;
  box-sizing: border-box;
  padding-right: 24px;
  color: white; /* 文字顏色，避免跟背景混在一起 */
  white-space: nowrap;
}

/* 跑馬燈動畫 */
@keyframes marquee {
  from {
    transform: translateX(0);
  }
  to {
    transform: translateX(-33.333%); /* 移動「三分之一」寬度 */
  }
}

.special-text {
  font-family: 'Saira', sans-serif;
  font-size: 1.1rem !important;
  white-space: nowrap;
}

@media (min-width: 992px) {
  .special-text {
    font-size: clamp(2rem, 3.2vw, 3rem) !important;
    font-weight: 700 !important;
  }

  .marquee.command-center-marquee {
    height: 80px;
  }

  .marquee.command-center-marquee .special-text {
    font-size: clamp(2.1rem, 3.3vw, 3rem) !important;
    font-weight: 500 !important;
  }
}

@media (min-width: 768px) and (max-width: 991.98px) {
  .special-text {
    font-size: 1.25rem !important;
  }
}

@media (max-width: 991.98px) {
  /* 讓每組文字依內容排列，縮短平板與手機版的重複間距。 */
  .marquee div:not(.marquee-bg) {
    display: flex;
    width: max-content;
  }

  .marquee span {
    float: none;
    width: auto;
    flex: 0 0 auto;
    padding-right: 16px;
  }
}

@media (max-width: 390px) {
  .marquee span {
    padding-right: 8px;
  }
}
</style>
