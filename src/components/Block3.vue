<script setup lang="ts"></script>

<template>
  <div class="outer-container position-relative d-flex justify-content-center">
    <img class="img" src="/desktop/about.png" alt="" />

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
      margin-top: 120px;
      width: 100%;
      height: 672px;
      object-fit: cover;
    }
    .content-container {
      padding: 80px;
      top: 200px;
      left: 564px;
      width: 54.38%;
      height: 672px;
      border-radius: 80px 80px 0px 80px;
      border-bottom: 1px solid var(--Neutral-0, #fff);
      border-left: 1px solid var(--Neutral-0, #fff);
      background: linear-gradient(180deg, rgba(20, 15, 10, 0.8) 0%, rgba(190, 156, 124, 0.8) 100%);
      backdrop-filter: blur(10px);
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
