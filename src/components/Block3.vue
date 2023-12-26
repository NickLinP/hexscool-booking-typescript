<script setup lang="ts">
import Pagination from '../components/Pagination.vue'
</script>

<template>
  <div class="outer-container position-relative d-flex justify-content-center">
    <div class="img position-absolute">
      <img class="w-100 h-100 position-absolute" src="/desktop/room1.png" alt="" />
      <Pagination />
    </div>

    <div>
      <img class="line position-absolute" src="/desktop/line3.png" alt="" />
      <img class="bg position-absolute" src="/desktop/bg.png" alt="" />
      <div class="content-container position-absolute">
        <p>尊爵雙人房</p>
        <p>享受高級的住宿體驗，尊爵雙人房提供給您舒適寬敞的空間和精緻的裝潢。</p>
        <p>NT$ 10,000</p>
        <button></button>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import '@/assets/scss/global.scss';
@import '@/assets/scss/BootstrapReset.scss';
@media (min-width: 1024px) {
  .outer-container {
    width: 100%;
    height: 1140px;
    .img {
      top: 120px;
      left: 0;
      width: 900px;
      height: 900px;
      object-fit: cover;
    }
    .line {
      top: 180px;
      right: 0;
      width: 1060px;
      height: 187px;
      object-fit: cover;
    }
    .bg {
      right: 0;
      bottom: 0;
      width: 100%;
      height: 677px;
      object-fit: cover;
    }
    .content-container {
      padding: 80px;
      bottom: 120px;
      right: 312px;
      width: 628px;
      height: 418px; 
      .title-container {
        .title {
          @include customTextStyle(48px, 57.6px, 700);
          color: #ffffff;
        }
        .hr-line {
          margin-left: 40px;
          width: 165px;
          height: 2px;
          background: linear-gradient(90deg, #fff 0%, #fff 100%);
        }
      }
      .content {
        @include customTextStyle(16px, 24px, 500);
        color: #ffffff;
      }
    }
  }
}
.outer-container {
  background-color: #000000;
}
</style>
