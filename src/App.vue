<script setup>
import { useRoute, useRouter } from 'vue-router'
import { useUserStore } from '@/stores/user'
const router = useRouter()
const route = useRoute()
const goList = () => {
  router.push('/list')
  console.log(router, route)
}
const userStore = useUserStore()
</script>

<template>
  <div>
    <div>111</div>
    <div>{{ userStore.token }}</div>
    <el-button @click="userStore.setToken('1232456')">登录</el-button>
    <el-button @click="userStore.removeToken()">退出</el-button>
    <button @click="goList">333</button>
  </div>
</template>

<style scoped></style>
