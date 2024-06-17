<template>
  <el-row class="prodect">
    <el-col :span="8" v-for="(item, k) in items" :key="k" class="list-style">
      <el-card :body-style="{ padding: '0px' }">
        <el-image class="image" :src="item.src" />
        <div style="padding: 14px">
          <span>{{ item.title }}</span>
          <div class="bottom">
            <time class="time">{{ item.desc }}</time>
            <el-button text class="button" link @click="tolink(item.id)" v-if="item.id==1">访问</el-button>
          </div>
        </div>
      </el-card>
    </el-col>
  </el-row>
  <el-drawer v-model="drawer" title="I am the title" :with-header="false">
    <!-- drawer弹窗内容开始 -->
    <h3>最新收录</h3>
    <el-card style="max-width: 480px">
      <el-tooltip
        class="box-item"
        effect="dark"
        placement="bottom"
        v-for="(i,k) in navItems" :key="k"
        :content="i.desc"
      >
        <el-link  :href="i.url" target="_blank">{{i.title}}</el-link>
      </el-tooltip>
      
    </el-card>
  </el-drawer>
</template>

<script setup>
import { ref } from 'vue'
import productData from '@/mock/product.json'
import navCodeData from '@/mock/navcode.json'

// 响应式变量
const drawer = ref(false)
const items = ref(productData)
const navItems = ref(navCodeData)

const tolink = (id) => {
  if(id==1){
    drawer.value = true
  }
  
}

</script>

<style>
.time {
  font-size: 12px;
  color: #999;
}

.bottom {
  margin-top: 13px;
  line-height: 12px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.button {
  padding: 0;
  min-height: auto;
}

.image {
  width: 100%;
  display: block;
  height: 7rem;
}

.list-style {
  padding: .5rem;
}

.el-link {
  margin-right: 8px;
}

@media (min-width: 1024px) {
  .product {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>

