<template>
  <section>
    <BaseDot text="設計目標" class="pb-12" />
    <div class="row g-12">
      <div v-for="step in props.steps" :key="step.stepNum" class="col-12 target-column d-flex">
        <TargetCardStep
          :title="step.title"
          :content="step.content"
          :step-num="step.stepNum"
          :img-url="step.img"
          :alt="step.alt"
        />
      </div>
    </div>
  </section>
</template>

<script setup>
import BaseDot from '@/components/Dot.vue'
import TargetCardStep from './TargetCardStep.vue'
const props = defineProps({
  steps: {
    type: Array,
    required: true,
    validator: (value) => {
      return value.every(
        (step) =>
          'title' in step &&
          'content' in step &&
          'stepNum' in step &&
          'img' in step &&
          'alt' in step,
      )
    },
  },
})
</script>

<style scoped>
.target-column {
  flex: 0 0 auto;
  width: 100%;
  align-items: stretch;
}

@media (min-width: 900px) {
  .target-column {
    width: 33.33333333%;
  }
}
</style>
