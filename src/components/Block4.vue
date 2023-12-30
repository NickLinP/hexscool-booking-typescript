<script setup lang="ts">
interface card {
  img: string
  name: string
  dateTime: string
  description: string
}
const foodArray: Array<card> = [
  {
    img: '/desktop/food1.png',
    name: '海霸',
    dateTime: 'SUN-MON 11:00 - 20:30',
    description:
      '以新鮮海產料理聞名，我們的專業廚師選用高雄當地的海鮮，每一道菜都充滿海洋的鮮美與清甜。無論是烤魚、蒸蝦還是煮蛤蜊，都能讓您品嚐到最新鮮的海洋風味。'
  },
  {
    img: '/desktop/food2.png',
    name: '日食',
    dateTime: 'SUN-MON 17:00 - 22:00',
    description:
      '為您提供優質的牛排，每一塊肉都來自頂級的牛肉，經過專業廚師的巧手烹調，口感豐滿、風味絕佳。搭配我們的特製醬料，讓您的味蕾享受一場美味的盛宴。'
  },
  {
    img: '/desktop/food3.png',
    name: '山臻',
    dateTime: 'SUN-MON 11:30 - 20:30',
    description:
      '帶您進入一次辣味與鮮香兼具的川菜美食之旅。我們的廚師掌握正宗的川菜烹調技巧，從麻辣鍋到口水雞，每一道菜都有其獨特的風味，讓您回味無窮。'
  },
  {
    img: '/desktop/food4.png',
    name: '月永',
    dateTime: 'SUN-MON 11:00 - 20:00',
    description:
      '從鮮美的海鮮、經典的牛排，到各國的特色美食，我們都一應俱全。在這裡，您可以品嚐到世界各地的美食，每一道菜都由專業廚師用心製作，讓您在享受美食的同時，也能感受到我們的熱情與用心。'
  },
  {
    img: '/desktop/food5.png',
    name: '天潮',
    dateTime: 'SUN-MON 14:00 - 19:30',
    description:
      '我們提供各種精緻甜點與糕點，無論您喜歡的是巧克力蛋糕、法式馬卡龍，還是台灣傳統的糕點，都能在這裡找到。讓我們的甜點帶您進入一場繽紛的甜蜜旅程。'
  }
]
</script>

<template>
  <div class="outer-container position-relative">
    <img class="img-line position-absolute" src="/desktop/line.png" alt="" />
    <img class="img-dot position-absolute" src="/desktop/dot.png" alt="" />

    <div class="inner-container">
      <div class="title-container d-flex justify-content-between align-items-center">
        <div class="title">
          <p>佳餚</p>
          <p>美食</p>
        </div>
        <div class="hr-line"></div>
      </div>
      <div class="cards-container d-flex position-relative">
        <div class="card" v-for="(item, index) in foodArray" :key="index">
          <img class="w-100 h-100" :src="item.img" alt="" />
          <div class="content position-absolute d-flex flex-column justify-content-between">
            <div class="d-flex justify-content-between align-items-center">
              <p class="name">{{ item.name }}</p>
              <p class="time">{{ item.dateTime }}</p>
            </div>
            <p class="description">
              {{ item.description }}
            </p>
          </div>
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
    height: 1040px;
    .img-line {
      width: 187px;
      height: 1068px;
      object-fit: cover;
      left: 40px;
      top: 50px;
      z-index: 1;
    }
    .img-dot {
      width: 200px;
      height: 200px;
      object-fit: cover;
      right: 80px;
      top: -40px;
      z-index: 1;
    }
    .inner-container::-webkit-scrollbar {
      display: none;
    }
    .inner-container {
      max-width: calc(100% - 312px);
      position: absolute;
      left: 312px;
      top: 120px;
      overflow-x: scroll;
      -ms-overflow-style: none; /* IE and Edge */
      scrollbar-width: none; /* Firefox */
      .title-container {
        width: 306px;

        .title {
          @include customTextStyle(48px, 57.6px, 700);
          color: $--primary-100;
        }
        .hr-line {
          width: 167px;
          height: 2px;
          background: linear-gradient(90deg, #be9c7c 0%, #fff 100%);
        }
      }
      .cards-container {
        margin-top: 80px;
        .card {
          width: 416px;
          min-width: 416px;
          height: 600px;
          margin-right: 24px;
          overflow: hidden;
          .content {
            background: linear-gradient(180deg, rgba(0, 0, 0, 0) 0%, #140f0a 77.6%);
            backdrop-filter: blur(10px);
            height: 197px;
            color: #ffffff;
            padding: 24px;
            bottom: 0;
            .name {
              @include customTextStyle(24px, 28.8px, 700);
            }
            .time {
              @include customTextStyle(16px, 24px, 700);
            }
            .description {
              @include customTextStyle(16px, 24px, 700);
            }
          }
        }
      }
    }
  }
}
.outer-container {
  background-color: #f7f2ee;
}
</style>
