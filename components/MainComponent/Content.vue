<template>
  <div class="main-wrapper">
    <div class="main-wrapper_title title">
      <p>Защищенный</p>
      <p>Быстрый</p>
      <p>Свободный</p>
    </div>
    <div class="main-wrapper__btn">
      <ButtonComponent :text="ButtonText" :link="LinkBot" />
    </div>
    <div class="main-wrapper_comet">
      <TitleStars />
    </div>
  </div>
</template>

<script setup>
import TitleStars from "./TitleStars.vue";
import ButtonComponent from "../UI/ButtonWhite.vue";

const ButtonText = "Попробовать сейчас";
const LinkBot = "http://t.me/KometaVPNBot";
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
  display: flex;
  flex-direction: column;
  padding-left: 5%;
  z-index: 1;
}

.main-wrapper_title ::first-letter {
  color: #38FA59;
}

.main-wrapper_title {
  font-size: calc(46px + (87 + 87 * 0.7) * ((100vw - 320px) / 1920));
  letter-spacing: 0;
  text-align: start;
}

.main-wrapper__btn {
  margin-top: 4.6vw;
}

.main-wrapper_comet {
  position: absolute;
  right: 25%;
  top: 25px;
  transform: translateX(-50%);
  z-index: -100;
}

.main-wrapper_btn-text {
  font-size: calc(18px + 6 * (100vw / 1920));
}

@media (max-width: 1476px) {
  .main-wrapper_comet {
    right: 45%;
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

  .main-wrapper__btn {
    margin-top: 6.6vw;
  }
}

@media (max-width: 422px) {
  .main-wrapper_title {
    font-size: 38px;
  }

  .main-wrapper_comet {
    right: 70%;
  }
  .main-wrapper__btn {
    margin-top: 10vw;
  }
}
</style>
