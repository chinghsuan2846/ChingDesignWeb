<template>
  <section>
    <BaseDot :text="props.title" class="pb-4" />
    <p class="pb-12 mb-0">
      {{ props.content }}
    </p>
    <div class="row gy-8 gx-16">
      <div v-for="question in props.questions" :key="question.num" class="col-12 col-md-6 d-flex">
        <QuestionDefineCard
          :title="question.title"
          :content="question.content"
          :num="question.num"
          :img-url="question.img"
          :alt="question.alt"
          :size="question.size"
          class="w-100"
        />
      </div>
    </div>
  </section>
</template>

<script setup>
import BaseDot from '@/components/Dot.vue'
import QuestionDefineCard from './QuestionDefineCard.vue'
const props = defineProps({
  title: { type: String, required: true, default: '問題定義' },
  questions: {
    type: Array,
    required: true,
    validator: (value) => {
      return value.every(
        (question) =>
          'title' in question &&
          'content' in question &&
          'num' in question &&
          'img' in question &&
          'alt' in question &&
          'size' in question,
      )
    },
  },
  content: { type: String, required: true },
})
</script>
