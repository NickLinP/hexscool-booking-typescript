<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import MainNavBar from '@/components/MainNavBar.vue'
</script>

<template>
  <MainNavBar />
  <RouterView />
</template>

<style lang="scss" scoped>
@import "@/assets/scss/global.scss";  
@media (min-width: 1024px) {
  
}
</style>
