<template>
  <section class="info_try-now justify-center">
    <div>
      <p class="title">Опробуй уже сейчас</p>
    </div>
    <div class="info_try-now__btn-wrapper justify-center">
      <ButtonWhite class="button-1" :text="TextBot" :link="LinkBot" />
      <ButtonBlack class="button-2" :text="TextExtention" />
    </div>
    <div>
      <p class="text">
        Пользуясь нашим сервисом вы соглашаетесь на <br />
        <NuxtLink to="about">
          <span class="confidentiality"> политику конфиденциальности и условия пользования </span>
        </NuxtLink>
      </p>
    </div>
  </section>
</template>

<script setup>
import ButtonBlack from "../UI/ButtonBlack.vue";
import ButtonWhite from "../UI/ButtonWhite.vue";

const TextBot = "Ссылка на телеграм бот";
const TextExtention = "Расширение для браузера";
const LinkBot = "http://t.me/KometaVPNBot";
</script>

<style scoped>
.info_try-now {
  margin-top: 400px;
  margin-bottom: 202px;
}

.info_try-now__btn-wrapper {
  margin-top: 5vw;
  flex-direction: column;
  gap: 10px;
}

.button-1 {
  width: 100%;
}

.text {
  margin-top: 10px;
}

.confidentiality {
  color: var(--sb-thumb-color);
  cursor: pointer;
}

@media (max-width: 574px) {
}
</style>
