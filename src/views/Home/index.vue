<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <!-- 头部组件 -->
    <AppHeader />
    <!-- 频道组件 -->
    <HomeChannel />

</template>

<script setup lang="ts">
// script setup 只需导入组件，无需注册
import AppHeader from '@/components/app-header.vue'
import HomeChannel from './components/home-channel.vue'
</script>
