<template>
  <Transition name="fade">
    <div :v-if="isVisible" class="fade-in" ref="el">
      <div class="info_we-believe">
        <div class="info_we-believe_title">
          <p>Цель проекта</p>
        </div>
        <div class="info_we-believe_desc">
          <p>
            Наш VPN сервис обеспечивает свободу доступа к информации, поддерживая принципы открытого интернета, о
            которых говорил Джон Перри Барлоу
          </p>
        </div>
      </div>
      <div class="info_we-believe_quote">
        <Comet class="info_we-believe_quote-1" />
        <div class="info_we-believe_quote-2">
          <p>
            «Моя родина — Киберпространство,<br />
            новый дом сознания».
          </p>
        </div>
        <Comet class="info_we-believe_quote-3" />
      </div>
    </div>
  </Transition>
</template>

<script setup>
import { ref } from "vue";
import { useIntersectionObserver } from "@vueuse/core";

const isVisible = ref(false);
const el = ref(null);

const { stop } = useIntersectionObserver(el, ([{ isIntersecting }]) => {
  if (isIntersecting && !isVisible.value) {
    isVisible.value = true;
    console.log(isVisible.value, "компонент в области видимости");
    stop();
  }
});
</script>

<style scoped>
.info_we-believe {
  justify-items: center;
  align-items: center;
  min-width: 320px;
  max-width: 100%;
  margin: auto;
}
.info_we-believe_title {
  font-size: calc(50px + (40 + 40 * 0.7) * ((100vw - 320px) / 1920));
  font-weight: 900;
  line-height: 85%;
  letter-spacing: -6%;
  font-style: italic;
}

.info_we-believe_desc {
  font-size: calc(18px + (6 + 6 * 0.7) * ((100vw - 320px) / 1920));
  margin-top: 5vw;
  text-align: center;
  max-width: 628px;
  min-width: 335px;
  font-weight: 400;
  letter-spacing: -3%;
}

.info_we-believe_quote {
  display: grid;
  grid-template-columns: repeat(5, auto);
  grid-template-rows: repeat(6, 50px);
  grid-auto-flow: column;
  height: 400px;
  gap: 51px;
  justify-content: center;
  font-size: calc(18px + (6 + 6 * 0.7) * ((100vw - 320px) / 1920));
  margin-top: 41px;
  font-weight: bolder;
  min-width: 335px;
  text-align: center;
}

.info_we-believe_quote-1 {
  grid-area: 1 / 1 / 6 / 1;
}

.info_we-believe_quote-2 {
  grid-area: 1 / 3 / 1 / 3;
}

.info_we-believe_quote-3 {
  grid-area: 1 / 6 / 6 / 5;
}

.comet {
  top: 30px;
}

/* анимация в облости видимости на экране */
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease-out;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}

.fade-in {
    opacity: 1;
}

@media (max-width: 847px) {
  .info_we-believe {
    justify-items: start;
    margin: auto;
    width: 100%;
    margin-left: 10px;
  }

  .info_we-believe_title {
    text-align: start;
  }

  .info_we-believe_desc {
    text-align: start;
  }

  .info_we-believe_quote {
    gap: 10px;
  }

  .info_we-believe_quote-1 {
    grid-area: 2 / 2 / 7 / 2;
  }

  .info_we-believe_quote-3 {
    grid-area: 2 / 4 / 7 / 4;
    justify-content: space-around;
  }
}
</style>
