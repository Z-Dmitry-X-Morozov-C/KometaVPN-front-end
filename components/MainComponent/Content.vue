<template>
  <div class="main-wrapper">
    <p class="main-wrapper_title title">
      Быстрый <br />
      Приватный <br />
      Свободный
    </p>
    <button class="main-wrapper_btn main-wrapper_btn-text">Попробовать сейчас</button>
    <div class="main-wrapper_comet">
      <TitleStars />
    </div>
  </div>
</template>

<script setup>
import TitleStars from "./TitleStars.vue";
</script>

<style scoped>
@keyframes stars-flow {
  from {
    transform: translatex(0) translatey(2%);
    opacity: 0;
  }
  to {
    transform: translatex(2%) translatey(0);
    opacity: 1;
  }
}
.main-wrapper {
  position: relative;
  margin: 0 5%;
  z-index: 1;
}

.main-wrapper_title {
  display: inline-block;
  font-size: calc(34px + 99 * (100vw / 1920));
  font-weight: 900;
  line-height: 85%;
  cursor: default;
  text-align: start;
}

.main-wrapper_comet {
  position: absolute;
  right: 30%;
  transform: translateX(-50%);
  top: 25px;
  z-index: -101;
}

.main-wrapper_btn {
  position: relative;
  display: flex;
  margin-top: 4.6vw;
  color: black;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding: 20px;
  border-radius: 12px;
  border: none;
  background: rgb(255, 255, 255);
  cursor: pointer;
}

.main-wrapper_btn-text {
  font-size: calc(18px + 6 * (100vw / 1920));
}

@media (max-width: 1476px) {
  .main-wrapper_comet {
    right: 40%;
  }
}

@media (max-width: 847px) {
  .main-title_text {
    font-size: calc(34px + (99 + 99 * 0.7) * ((100vw - 375px) / 1920));
  }

  .main-wrapper {
    position: relative;
  }

  .main-wrapper_comet {
    scale: 1.3;
    top: 60%;
    right: 60%;
  }

  .main-wrapper_btn {
    padding: 16px;
  }

  .main-wrapper_btn-text {
    font-size: calc(18px + (6 + 6 * 0.7) * ((100vw - 375px) / 847px));
  }
}

@media (max-width: 422px) {
  .main-wrapper_comet {
    right: 70%;
  }
  .main-wrapper_btn {
    margin-top: 48px;
  }
}

</style>
