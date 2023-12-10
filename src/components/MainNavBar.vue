<script setup lang="ts">
// defineProps<{
//   msg: string
// }>()
</script>

<template>
  <nav>
    <div class="outer-container">
      <div class="main-navbar d-flex justify-content-between align-items-center">
        <img src="@/assets/img/MainNavBar/logo.svg" alt="" />
        <div>
          <div class="btn-container d-flex justify-content-between align-items-center">
            <RouterLink class="nav-item text-light text-decoration-none d-flex justify-content-center  align-items-center h-100" to="/about">客房旅宿</RouterLink>
            <RouterLink class="nav-item text-light text-decoration-none d-flex justify-content-center align-items-center h-100" to="/about">會員登入</RouterLink>
            <RouterLink class="go-to-booking btn-primary-100 text-light text-decoration-none d-flex justify-content-center align-items-center h-100" to="/about">立即訂房</RouterLink>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>

<style scoped>
@import "@/assets/scss/global.scss";  
@media (min-width: 1024px) {
  .outer-container {
    padding: 24px 80px;
    position: fixed;
    width: 100%;

    .btn-container {
      width: 355px;
      height: 56px;
      .nav-item{
        width: 97px;
      }
      .go-to-booking{
        width: 129px;
      }
    }
  }
}

.main-navbar {
}
</style>
