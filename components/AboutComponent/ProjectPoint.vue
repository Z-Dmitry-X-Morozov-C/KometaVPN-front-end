<template>
  <Transition name="fade">
    <div :v-if="isVisible" class="fade-in" ref="el">
      <div class="info_project_point justify-center">
        <div class="info_project_point_title">
          <p class="title">Цель проекта</p>
        </div>
        <div class="info_project_point_desc">
          <p class="text">
            Наш VPN сервис обеспечивает свободу доступа к информации, поддерживая принципы открытого интернета, о
            которых говорил Джон Перри Барлоу
          </p>
        </div>
      </div>
      <div class="info_project_point_quote">
        <Comet class="info_project_point_quote-1" />
        <div class="info_project_point_quote-2">
          <p>
            «Моя родина — Киберпространство,<br />
            новый дом сознания».
          </p>
        </div>
        <Comet class="info_project_point_quote-3" />
      </div>
    </div>
  </Transition>
</template>

<script setup>
import "~/assets/styles.css";
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
.info_project_point_desc {
  margin-top: 5vw;
  max-width: 628px;
  min-width: 335px;
  text-align: center;
}

.info_project_point_quote {
  display: grid;
  grid-template-columns: repeat(3, auto);
  grid-template-rows: repeat(3, 50px);
  grid-auto-flow: column;
  height: 400px;
  gap: 51px;
  justify-content: center;
  font-size: calc(18px + (6 + 6 * 0.7) * ((100vw - 320px) / 1920));
  margin-top: 41px;
  font-weight: bolder;
  min-width: 335px;
  text-align: center;
  line-height: 130%;
}

.info_project_point_quote-1 {
  grid-area: 1 / 1 / 6 / 1;
}

.info_project_point_quote-2 {
  grid-area: 1 / 2 / 1 / 2;
}

.info_project_point_quote-3 {
  grid-area: 1 / 3 / 6 / 3;
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
  .info_project_point {
    justify-items: start;
    margin: auto;
    width: 100%;
    margin-left: 10px;
  }

  .info_project_point_title {
    text-align: start;
  }

  .info_project_point_desc {
    text-align: start;
  }

  .info_project_point_quote {
    gap: 10px;
  }

  .info_project_point_quote-1 {
    grid-area: 2 / 2 / 5 / 2;
    margin-left: 20px;
  }

  .info_project_point_quote-3 {
    grid-area: 2 / 2 / 5 / 2;
    justify-self: end;
    margin-right: 20px;
  }
}
</style>
