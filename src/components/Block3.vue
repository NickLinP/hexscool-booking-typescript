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
        <p class="title">尊爵雙人房</p>
        <p class="description">
          享受高級的住宿體驗，尊爵雙人房提供給您舒適寬敞的空間和精緻的裝潢。
        </p>
        <p class="price">NT$ 10,000</p>
        <div class="see-more d-flex justify-content-end align-items-center">
          <p class="content">立即訂房</p>
          <div class="hr-line"></div>
        </div>
        <div class="arrows d-flex justify-content-end">
          <img src="/desktop/arrow_left.svg" alt="" /><img src="/desktop/arrow_right.svg" alt="" />
        </div>
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
      z-index: 1;
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
      bottom: 120px;
      right: 312px;
      width: 628px;
      height: 418px;
      z-index: 2;
      .title {
        @include customTextStyle(48px, 48px, 700);
        color: #ffffff;
      }
      .description {
        @include customTextStyle(16px, 24px, 500);
        color: #ffffff;
        margin-top: 16px !important;
      }
      .price {
        @include customTextStyle(32px, 38.4px, 700);
        color: #ffffff;
        margin-top: 40px !important;
      }
      .see-more:hover {
        background-color: $--primary-100;
        .content {
          color: #ffffff;
        }
        .hr-line {
          background-color: #ffffff;
        }
      }
      .see-more {
        width: 628px;
        height: 116px;
        @include customTextStyle(24px, 36px, 700);
        color: #000000;
        border-radius: 8px;
        background-color: #ffffff;
        border: none;
        padding: 40px;
        margin-top: 40px !important;
        .content {
          @include customTextStyle(24px, 36px, 700);
          margin-right: 16px !important;
        }
        .hr-line {
          width: 150px;
          height: 1px;
          background-color: #000000;
        }
      }
      .arrows{
        margin-top: 40px !important;
      }
    }
  }
}
.outer-container {
  background-color: #000000;
}
</style>
