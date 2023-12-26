<script setup lang="ts">
import Pagination from '../components/Pagination.vue'
</script>

<template>
  <div class="background-image position-relative">
    <div class="inner-container position-absolute">
      <div class="d-flex title-container">
        <div class="title text-primary-100">
          <div class="title-name">享樂酒店</div>
          <div class="title-name-en">Enjoyment Luxury Hotel</div>
          <div class="hr-line"></div>
        </div>
      </div>
      <div class="description-outer-container">
        <div class="description-container">
          <p class="title">高雄</p>
          <p class="title" style="margin-top: 8px">豪華住宿之選</p>
          <p class="description">我們致力於為您提供無與倫比的奢華體驗與優質服務</p>
          <div class="btn-booking d-flex justify-content-end align-items-center">
            <p class="content">立即訂房</p>
            <div class="hr-line"></div>
          </div>
        </div>
      </div>
    </div>

    <Pagination />
  </div>
</template>

<style lang="scss" scoped>
@import '@/assets/scss/global.scss';
@import '@/assets/scss/BootstrapReset.scss';
@media screen and (min-width: 768px) {
  .inner-container {
    width: 91.67%;
    height: 678px;
    top: 236px;
    left: 50%;
    transform: translateX(-50%);
    .title-container {
      width: 47.5%;
      .title {
        position: absolute;
        top: 50%;
        transform: translateY(-50%);

        .title-name {
          @include customTextStyle(40px, 48px, 700);
        }
        .title-name-en {
          margin-top: 8px;
          @include customTextStyle(24px, 28.8px, 700);
        }
        .hr-line {
          margin-top: 40px;
          background: linear-gradient(90deg, #be9c7c 0%, #fff 100%);
          width: 636px;
          height: 2px;
        }
      }
    }
    .description-outer-container {
      position: absolute;
      right: 0;
      width: 52.5%;
      height: 678px;
      border-radius: 80px;
      border-top: 1px solid #f5f7f9;
      border-right: 1px solid #f5f7f9;
      background: linear-gradient(180deg, rgba(255, 255, 255, 0) 0%, rgba(255, 255, 255, 0.3) 100%);
      backdrop-filter: blur(10px);
      .description-container {
        position: absolute;
        top: 96px;
        left: -48px;

        .title {
          @include customTextStyle(100px, 120px, 700);
          color: #ffffff;
        }
        .description {
          margin-top: 24px;
          @include customTextStyle(32px, 38.4px, 600);
          color: #ffffff;
        }
        .btn-booking:hover {
          background-color: $--primary-100;
          .content {
            color: #ffffff;
          }
          .hr-line {
            background-color: #ffffff;
          }
        }
        .btn-booking {
          width: 772px;
          height: 116px;
          border-radius: 8px;
          background-color: #ffffff;
          margin-top: 60px;
          padding: 40px;
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
      }
    }
  }
}
.background-image {
  width: 100%;
  height: 1080px;
  background-image: url('/desktop/banner.png');
  background-position: center center;
  background-size: cover;
}
</style>
