<template>
  <div class="info_try-now justify-center">
    <div>
      <p class="title">Опробуй уже сейчас</p>
    </div>
    <div>
      <ButtonComponent :text="Buttontext" />
    </div>
  </div>
</template>

<script setup>
import ButtonComponent from "../UI/ButtonComponent.vue";

const Buttontext = "Ссылка на телеграм бот";
</script>

<style scoped>
.info_try-now {
  margin-top: 400px;
  padding-bottom: 202px;
}
</style>
