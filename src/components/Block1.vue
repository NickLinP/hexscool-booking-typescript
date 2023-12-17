<script setup lang="ts"></script>

<template>
  <div class="outer-container position-relative d-flex justify-content-center">
    <!-- 最新消息 -->
    <div class="title-container">
      <p class="title">最新</p>
      <p class="title" style="margin-top: 4px">消息</p>
      <div class="hr-line"></div>
    </div>
    <!-- 卡片容器 -->
    <div class="card-container">
      <div class="card d-flex flex-row justify-content-between align-items-center">
        <img src="/desktop/news1.png" class="img" />
        <div class="content-container">
          <p class="title">秋季旅遊，豪華享受方案</p>
          <p class="content">
            秋天就是要來場豪華的旅遊！我們為您準備了一系列的秋季特別方案，包括舒適的住宿、美食饗宴，以及精彩的活動。不論您是想來一趟浪漫之旅，還是想和家人共度美好時光，都能在這裡找到最適合的方案。
          </p>
        </div>
      </div>
      <div class="card gap d-flex flex-row justify-content-between align-items-center">
        <img src="/desktop/news2.png" class="img" />
        <div class="content-container">
          <p class="title">輕鬆住房專案</p>
          <p class="content">
            我們知道，有時候您只是需要一個舒適的地方放鬆心情。因此，我們推出了「輕鬆住房專案」，讓您無壓力地享受住宿。不管是短期的休息，還是長期的住宿，我們都會以最貼心的服務，讓您感到賓至如歸。
          </p>
        </div>
      </div>
      <div class="card gap d-flex flex-row justify-content-between align-items-center">
        <img src="/desktop/news3.png" class="img" />
        <div class="content-container">
          <p class="title">耶誕快樂，住房送禮</p>
          <p class="content">
            聖誕節來臨，我們為您準備了特別的禮物！在聖誕期間訂房，不僅有特別優惠，還會送上我們精心準備的聖誕禮物。讓我們一起慶祝這個溫馨的節日吧！
          </p>
        </div>
      </div>
    </div>
    <img src="/desktop/dot.png" class="dot dot-0 position-absolute" alt="" />
    <img src="/desktop/dot.png" class="dot dot-1 position-absolute" alt="" />
  </div>
</template>

<style lang="scss" scoped>
@import '@/assets/scss/global.scss';
@import '@/assets/scss/BootstrapReset.scss';
@media (min-width: 1024px) {
  .outer-container {
    padding: 120px 0;
    .title-container {
      width: 140px;
      margin-right: 80px;
      .title {
        @include customTextStyle(48px, 57.6px, 700);
        color: $--primary-100;
      }
      .hr-line {
        margin-top: 40px;
        width: 140px;
        height: 2px;
        background: linear-gradient(90deg, #be9c7c 0%, #fff 100%);
      }
    }
    .card-container {
      width: 1076px;
      .card {
        border: none;
        .img {
          width: 474px;
          height: 294px;
          border-radius: 8px;
          object-fit: cover;
          margin-right: 24px;
        }
      }
      .content-container {
        .title {
          @include customTextStyle(32px, 38.4px, 700);
        }
        .content {
          margin-top: 24px !important;
          @include customTextStyle(16px, 24px, 500);
          color: $--Neutral-80;
        }
      }
    }
    .dot {
      width: 200px;
      height: 200px;
      z-index: 1;
    }
    .dot-0 {
      top: 100px;
      right: 180px;
    }
    .dot-1 {
      left: 200px;
      bottom: -80px;
    }
  }
}

.outer-container {
  background-color: $--Primary-10;
  width: 100%;
  height: 1202px;
}
.card {
  background-color: $--Primary-10;
}
.gap {
  margin-top: 40px !important;
}
</style>
