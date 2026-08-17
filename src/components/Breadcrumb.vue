<script setup>
defineOptions({ name: 'AppBreadcrumb' })
import { ref, watch } from 'vue'
import { useRoute, RouterLink } from 'vue-router'

const route = useRoute()
const paths = ref(['Home', ...route.path.split('/').filter(Boolean)])

const getPath = (index) => {
  if (index === 0) return '/'
  const path = paths.value.slice(1, index + 1)
  console.log('getPath', path)
  return '/' + path.join('/')
}
const pathChineseMap = {
  lineLiff: '星舟快充 LINE Liff 設計',
  chargingStation: '智慧開電選址系統',
  commandCenterDashboard: '能源戰情系統展示牆',
  platformRedesign: '綠電平台視覺與架構優化',
  eomc: '企業營運中心管理系統',
}

watch(
  () => route.path,
  (newPath) => {
    paths.value = ['Home', ...newPath.split('/').filter(Boolean)]
  },
)
</script>

<template>
  <nav v-if="paths.length > 1" aria-label="breadcrumb" class="container background">
    <ol class="breadcrumb mb-0">
      <li
        v-for="(path, index) in paths"
        :key="index"
        class="breadcrumb-item"
        :class="{ active: index === paths.length - 1 }"
        aria-current="page"
      >
        <template v-if="index === paths.length - 1">
          <span class="text-success">{{ pathChineseMap[path] || path }}</span>
        </template>
        <template v-else>
          <RouterLink :to="getPath(index)" class="text-decoration-none">
            {{ path }}
          </RouterLink>
        </template>
      </li>
    </ol>
  </nav>
</template>

<style scoped>
* {
  font-weight: 400;
  font-size: 14px;
  line-height: 170%;
  letter-spacing: 2%;
}
.breadcrumb-item + .breadcrumb-item::before {
  content: '/';
  color: #d1d9e7; /* 這裡是斜線的顏色 */
}
nav {
  padding-top: 134px;
}
</style>
