<template>
  <div class="info_we-believe justify-center">
    <div class="info_we-believe_title title">
      <p>
        Мы верим, что <span class="title-style">интернет</span> должен быть пространством
        <span class="title-style">без цензуры</span>
      </p>
    </div>
    <div class="info_we-believe_desc">
      <p class="text">
        Где люди могут свободно обмениваться знаниями и идеями, оставаясь анонимными и защищёнными от внешнего контроля
      </p>
    </div>
  </div>
</template>

<script>
import "~/assets/styles.css";
</script>

<style scoped>
.info_we-believe {
  margin: 5px;
  margin-top: 20vw;
  gap: 2.8vw;
}

.info_we-believe_title {
  min-width: 320px;
  max-width: 1725px;
}

.info_we-believe_desc {
  max-width: 628px;
  min-width: 335px;
}

@media (max-width: 847px) {
  .info_we-believe_title {
    text-align: start;
  }

  .info_we-believe_desc {
    align-self: start;
  }
  .title-style {
    color: #ff6161;
  }
}
@media (max-width: 422px) {
  .info_we-believe {
    text-align: start;
  }

  .info_we-believe_title {
    text-align: start;
    font-size: 34px;
  }
}
</style>
