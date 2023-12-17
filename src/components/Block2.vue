<script setup lang="ts"></script>

<template>
  <div class="outer-container position-relative d-flex justify-content-center">
    <img class="img" src="/desktop/about.png" alt="" />
    <div class="content-container position-absolute">
      <div class="d-flex align-items-center">
        <div class="title-container d-flex align-items-center">
          <div>
            <p class="title">關於</p>
            <p class="title" style="margin-top: 4px">我們</p>
          </div>
          <div class="hr-line"></div>
        </div>
      </div>
      
      <div class="content" style="margin-top: 80px">
        享樂酒店，位於美麗島高雄的心臟地帶，是這座城市的璀璨瑰寶與傲人地標。
        我們的存在，不僅僅是為了提供奢華的住宿體驗，更是為了將高雄的美麗與活力，獻給每一位蒞臨的旅客。
      </div>
      <div class="content" style="margin-top: 40px">
        我們的酒店，擁有時尚典雅的裝潢，每一個細節都充滿著藝術與設計的精緻。
        我們的員工，都以熱情的服務與專業的態度，讓每一位客人都能感受到賓至如歸的溫暖。
      </div>
      <div class="content" style="margin-top: 40px">
        在這裡，您可以遙望窗外，欣賞高雄的城市景色，感受這座城市的繁華與活力；您也可以舒適地坐在我們的餐廳，品嚐精緻的佳餚，體驗無與倫比的味覺盛宴。
      </div>
      <div class="content" style="margin-top: 40px">
        享樂酒店，不僅是您在高雄的住宿之選，更是您感受高雄魅力的最佳舞台。我們期待著您的蒞臨，讓我們共同編織一段難忘的高雄故事。
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
    height: 992px;
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
