<template>
  <section>
    <BaseDot text="資訊架構" class="pb-4" />
    <p class="pb-12 mb-0">
      {{ props.content }}
    </p>
    <div class="site-map-frame border border-1 border-light bg-info">
      <img :src="imgUrl" :alt="alt" class="site-map-img" />
    </div>
  </section>
</template>

<script setup>
import BaseDot from '@/components/Dot.vue'
const props = defineProps({
  content: { type: String, required: true },
  imgUrl: { type: String, required: true },
  alt: { type: String, default: 'image' },
})
</script>

<style scoped>
.site-map-img {
  width: 90%;
  height: 90%;
  object-fit: contain;
  display: block;
}

.site-map-frame {
  width: 100%;
  aspect-ratio: 3.05;
  border-radius: 10px;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
