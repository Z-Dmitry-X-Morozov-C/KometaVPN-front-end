<template>
  <section class="info_try-now justify-center">
    <div>
      <p class="title">Опробуй уже сейчас</p>
    </div>
    <div class="info_try-now__btn justify-center">
      <ButtonWhite :text="TextBot" :link="LinkBot" />
      <ButtonBlack class="button_tranperent" :text="TextExtention" :link="LinkBot" />
    </div>
    <div>
      <p class="text">
        Пользуясь нашим сервисом вы соглашаетесь на <br />
        <span class="confidentiality"> политику конфиденциальности и условия пользования </span>
      </p>
    </div>
  </section>
</template>

<script setup>
import ButtonBlack from "../UI/ButtonBlack.vue";
import ButtonWhite from "../UI/ButtonWhite.vue";
import ButtonComponent from "../UI/ButtonWhite.vue";
import { ref } from "vue";

const TextBot = "Ссылка на телеграм бот";
const TextExtention = "Расширение для браузера";
const LinkBot = "http://t.me/KometaVPNBot";
</script>

<style scoped>
.info_try-now {
  margin-top: 400px;
  margin-bottom: 202px;
}

.info_try-now__btn {
  margin-top: 5vw;
  flex-direction: row;
  gap: 10px;
}

.text {
  margin-top: 10px;
}

.confidentiality {
  color: var(--sb-thumb-color);
  cursor: pointer;
}
</style>
