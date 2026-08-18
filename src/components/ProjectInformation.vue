<template>
  <section>
    <BaseDot text="專案資訊" />
    <hr class="mt-8 mb-6" />
    <div class="row">
      <div class="col-6 d-md-flex">
        <h4 class="fw-medium fs-9 lh-170">擔任角色</h4>
        <p class="ps-md-16">{{ props.role }}</p>
      </div>
      <div class="col-6 d-md-flex">
        <h4 class="fw-medium fs-9 lh-170">{{ props.durationLabel }}</h4>
        <p class="ps-md-16">{{ props.projectDuration }}</p>
      </div>
      <div class="col-6 d-md-flex">
        <h4 class="fw-medium fs-9 lh-170">使用工具</h4>
        <ul>
          <li v-for="(tool, index) in props.tools" :key="index">{{ tool }}</li>
        </ul>
      </div>
      <div class="col-6 d-md-flex">
        <h4 class="fw-medium fs-9 lh-170">負責項目</h4>
        <ul>
          <li v-for="(task, index) in props.tasks" :key="index">{{ task }}</li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script setup>
import BaseDot from '@/components/Dot.vue'
const props = defineProps({
  role: { type: String, required: true },
  projectDuration: { type: String, required: true },
  durationLabel: { type: String, default: '專案時間' },
  tools: { type: Array, required: true },
  tasks: { type: Array, required: true },
  imgUrl: { type: String, required: true },
  alt: { type: String, default: 'image' },
})
</script>

<style scoped>
ul {
  padding-left: 56px;
}

@media (max-width: 768px) {
  ul {
    padding-left: 20px;
  }
}
</style>
