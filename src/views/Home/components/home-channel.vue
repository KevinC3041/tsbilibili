<template>
  <van-tabs v-model:active="active">
    <van-tab title="tab 1" name="a">content of tab 1</van-tab>
    <van-tab title="tab 2" name="b">content of tab 2</van-tab>
    <van-tab title="tab 3" name="c">content of tab 3</van-tab>
    <van-tab title="tab 4" name="d">content of tab 4</van-tab>
  </van-tabs>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import axios from 'axios'
const active = ref(0)

interface INvaItem{
    id: string
    text: string
}
const list = ref<INvaItem[]>([])
</script>
