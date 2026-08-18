<template>
  <div class="card bg-warning border-0 target-card">
    <div class="card-body p-8">
      <span class="fw-medium fs-7 text-primary">{{ props.stepNum }}</span>
      <div class="d-flex flex-column align-items-center">
        <div class="bg-white rounded-circle mb-12">
          <img :src="imgUrl" :alt="alt" class="p-4 icon-img" />
        </div>
        <h4 class="card-title text-success fw-medium pb-2 fs-9 lh-170">
          {{ props.title }}
        </h4>
        <p class="card-text text-center">
          {{ props.content }}
        </p>
      </div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  title: { type: String, required: true },
  stepNum: { type: String, required: true },
  content: { type: String, required: true },
  imgUrl: { type: String, required: true },
  alt: { type: String, default: 'image' },
})
</script>

<style scoped>
p {
  line-height: 170%;
}
.icon-img {
  width: 72px;
  height: 72px;
}
.target-card {
  border-radius: 8px;
  width: 100%;
  height: 100%;
}
</style>
