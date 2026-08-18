<template>
  <div class="card border-0 bg-warning problem-card">
    <div class="card-body p-8 row g-12 justify-content-between">
      <div class="col-12 col-md-7">
        <div class="card-title pb-10 mb-0">
          <span
            class="step-number fw-bold d-inline-flex justify-content-center align-items-center rounded-circle bg-success text-white lh-140"
          >
            {{ num }}
          </span>
          <h4 class="d-inline-block ps-4 text-success fw-bold lh-140 fs-9">
            {{ title }}
          </h4>
        </div>
        <p class="card-text lh-base">{{ content }}</p>
      </div>

      <div class="col-12 col-md-5 d-flex align-items-center">
        <div
          class="problem-image-box rounded-3 d-flex justify-content-center align-items-center w-100 bg-white"
        >
          <img :src="imgUrl" :alt="alt" :class="['problem-img', sizeClass]" class="rounded-3" />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { computed } from 'vue'

const props = defineProps({
  num: Number,
  title: String,
  content: String,
  imgUrl: String,
  alt: String,
  size: {
    type: String,
    default: 'normal', // normal | small | large
    validator: (val) => ['normal', 'small', 'large'].includes(val),
  },
})

const sizeClass = computed(() => {
  return {
    'small-img': props.size === 'small',
    'large-img': props.size === 'large',
  }
})
</script>

<style scoped>
.problem-image-box {
  aspect-ratio: 200 / 168;
  overflow: hidden;
}
.step-number {
  width: 28px;
  height: 28px;
}
.problem-img {
  width: 100%;
  height: 100%;
  max-width: none;
  max-height: none;
  object-fit: contain;
  display: block;
}

.problem-img.small-img,
.problem-img.large-img {
  width: 100%;
  height: 100%;
}
</style>
