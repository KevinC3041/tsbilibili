<template>
  <van-tabs v-model:active="active">
    <van-tab v-for="item in list" :key="item.id" :title="item.text" name="a"></van-tab>
  </van-tabs>
</template>

<script setup lang="ts">
// TypeScript 的接口用于标记数据格式
import { ref } from 'vue'
import axios from 'axios'

interface INvaItem{
  id: string
  text: string
}

const active = ref(0)
// 频道数据，TypeScript <INavItem[]> 表示list数据为数组，数组的每一项需要符合INavItem接口的格式
// pros，模板中使用list和item的时候，鼠标移入有类型提醒
const list = ref<INvaItem[]>([])

axios({
  url: '/navList',
  method: 'get'
}).then(res => {
  console.log(res.data)
  list.value = res.data.result
})
</script>
