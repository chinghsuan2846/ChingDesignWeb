<template>
  <section class="others" :class="bgClass">
    <div class="container-xl">
      <div class="row">
        <div class="col-12 col-lg-3 d-flex flex-column align-items-center mb-6 mb-lg-0">
          <div class="d-flex pb-16">
            <span class="text-bar"></span>
            <div class="text-center text-md-start">
              <p class="mb-2">感謝觀看</p>
              <h4 class="fs-7 fw-medium text-success">查看其他作品</h4>
            </div>
          </div>
          <CustomButton>查看更多</CustomButton>
        </div>

        <div class="col-12 col-lg-9">
          <div class="row">
            <div class="col-6">
              <RouterLink :to="route1" class="other-work-link">
                <img :src="imgUrl1" :alt="alt1" class="img-fluid img-others" />
              </RouterLink>
            </div>
            <div class="col-6">
              <RouterLink :to="route2" class="other-work-link">
                <img :src="imgUrl2" :alt="alt2" class="img-fluid img-others" />
              </RouterLink>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import CustomButton from '@/components/Button.vue'
import { RouterLink } from 'vue-router'

defineProps({
  imgUrl1: { type: String, required: true },
  alt1: { type: String, default: 'image1' },
  route1: { type: String, required: true },
  imgUrl2: { type: String, required: true },
  alt2: { type: String, default: 'image2' },
  route2: { type: String, required: true },
  bgClass: { type: [String, Array, Object], default: 'bg-info' }, // 👉 新增背景 class 控制
})
</script>

<style scoped>
.others {
  width: 100%;
  position: relative;
  z-index: 10;
  padding: 100px 106px;
}

@media (max-width: 992px) {
  .others {
    padding: 80px 32px 100px;
  }
}

.img-others {
  display: block;
  width: 100%;
  transition: transform 280ms ease;
}
.other-work-link {
  display: block;
  overflow: hidden;
  border-radius: 8px;
  transition: box-shadow 280ms ease;
}
.other-work-link:hover .img-others,
.other-work-link:focus-visible .img-others,
.other-work-link:active .img-others {
  transform: scale(1.08);
}
.other-work-link:hover,
.other-work-link:focus-visible,
.other-work-link:active {
  box-shadow: 0 10px 24px rgba(37, 38, 45, 0.16);
}
.text-bar {
  display: block;
  width: 4px;
  background-color: #eaf0f6;
  margin-right: 12px;
}
</style>
