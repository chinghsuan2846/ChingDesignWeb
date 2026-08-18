<template>
  <div class="head bg-danger background">
    <div class="fixed-icon-1">
      <img src="/Profile/BG.png" alt="icon-1" />
    </div>
    <div class="fixed-icon-2">
      <img src="/Profile/BG.png" alt="icon-2" />
    </div>
    <div class="container-xl">
      <div>
        <h2 class="text-dark h1 pb-8 mb-0 fw-medium">Work</h2>
        <div class="row g-5 pb-16 justify-content-between">
          <div class="col-12 col-lg-5">
            <span class="button border border-1 border-success text-success lh-170">
              {{ props.tag }}
            </span>
            <h3 class="title text-success mb-0 pt-4 fw-medium">{{ props.title }}</h3>
            <p class="pt-16">
              {{ props.content }}
            </p>
          </div>
          <div class="col-12 col-lg-7">
            <img
              :src="imgUrl"
              :alt="alt"
              class="img-fluid border border-1 border-secondary img-rounded"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  title: { type: String, required: true },
  content: { type: String, required: true },
  tag: { type: String, required: true },
  imgUrl: { type: String, required: true },
  alt: { type: String, default: 'image' },
})
</script>

<style scoped>
.fixed-icon-1 {
  position: fixed;
  bottom: -15%;
  left: -5%;
  z-index: -1;
  pointer-events: none; /* 不影響點擊 */
}

.fixed-icon-1 img {
  width: 40%;
  animation: floatUpDown 2s infinite;
}

.fixed-icon-2 {
  position: fixed;
  top: 5%;
  right: -40%;
  z-index: -1;
  pointer-events: none; /* 不影響點擊 */
}

.fixed-icon-2 img {
  width: 50%;
  animation: floatUpDown 3s infinite;
}

.title {
  font-size: 1.5rem; /* 手機 */
}

@media (min-width: 768px) {
  .title {
    font-size: 1.75rem; /* md */
  }
}

@media (min-width: 992px) {
  .title {
    font-size: 2.25rem; /* lg */
  }
}

@keyframes floatUpDown {
  0% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-20px);
  }
  100% {
    transform: translateY(0);
  }
}

h3 {
  font-size: 36px;
}
p {
  line-height: 170%;
  color: #25262d;
}
.head {
  height: 85vh;
  position: sticky;
  top: 0;
  z-index: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

@media (max-width: 991.98px) {
  .head {
    height: auto;
    min-height: 85vh;
    padding: 72px 0 48px;
  }

  .head .container-xl {
    padding-left: 24px;
    padding-right: 24px;
  }
}
.button {
  border-radius: 100px;
  padding: 6px 20px;
}
.img-rounded {
  border-radius: 24px;
}
</style>
