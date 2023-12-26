<script setup lang="ts">
</script>

<template>
  <div class="pagination d-flex justify-content-between">
    <div class="active"></div>
    <div class="item"></div>
    <div class="item"></div>
    <div class="item"></div>
    <div class="item"></div>
  </div>
</template>

<style lang="scss" scoped>
@import '@/assets/scss/global.scss';
@import '@/assets/scss/BootstrapReset.scss';
@media (min-width: 1024px) {
  .pagination {
    position: absolute;
    left: 50%;
    right: 50px;
    transform: translate(-50%, -50%);
    bottom: 32px;
    width: 220px;
    .active {
      cursor: pointer;
      width: 60px;
      height: 4px;
      border-radius: 100px;
      background-color: $--primary-100;
    }
    .item {
      cursor: pointer;
      width: 32px;
      height: 4px;
      border-radius: 100px;
      background-color: #ffffff;
    }
  }
}
</style>
