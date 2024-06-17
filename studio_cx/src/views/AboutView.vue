<template>
  <div class="about">
    <el-timeline>
      <el-timeline-item v-for="(item, k) in items" :key="k" :timestamp="item.date" placement="top" :color="item.color">
        <el-card>
          <h3>{{ item.title }}</h3>
          <p>{{ item.desc }}</p>
        </el-card>
      </el-timeline-item>
    </el-timeline>
  </div>
</template>

<script>
import { ref } from 'vue'
import TimelineData from '@/mock/timeline.json'
export default {
  setup() {

    const items = ref(TimelineData)
    // 不要忘记同时暴露 increment 函数
    return {
      items,
    }
  }
}

</script>
<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
