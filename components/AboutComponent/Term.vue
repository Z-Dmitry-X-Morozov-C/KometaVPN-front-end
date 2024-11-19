<template>
  <div class="info_term justify-center">
    <div class="align-start">
      <p class="title">До 3-х</p>
      <p class="text m-top">Устройств</p>
    </div>
    <div class="align-start">
      <p class="title">30 дней</p>
      <p class="text m-top">Бесплатного пробного периода</p>
    </div>
    <div class="align-start">
      <p class="title">90 ₽</p>
      <p class="text m-top">В месяц</p>
    </div>
  </div>
</template>

<script setup></script>

<style scoped>
.info_term {
    margin-top: 400px;
  gap: 5vw;
}

.m-top {
  margin-top: 1vw;
}

@media (max-width: 422px) {
.justify-center {
  align-items: start;

}

  .title {
    text-align: start;
  }
  .text {
    text-align: start;
  }
}
</style>
