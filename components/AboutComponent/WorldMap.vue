<template>
  <div class="info_world-map justify-center">
    <div>
      <p class="title">Мы везде</p>
    </div>
    <div class="map_conteiner justify-center">
      <img src="../../assets/img/WorldMap.svg" alt="map" class="map" />
    </div>
    <div class="wrapper_countries_Netherlands">
      <p class="text">Нидерланды</p>
    </div>
    <div class="wrapper_countries_Norway">
      <p class="text">Норвегия</p>
    </div>
    <div class="wrapper_countries_Georgia">
      <p class="text">Грузия</p>
    </div>
    <div class="wrapper_countries_Hong-Kong">
      <p class="text">Гонконг</p>
    </div>
  </div>
</template>

<style scoped>
.info_world-map {
  margin: 250px;
  position: relative;
}

.map_conteiner {
  width: 100%;
}

.map {
  max-width: 100%;
  height: auto;
}

.wrapper_countries_Netherlands {
  position: absolute;
  top: 191px;
  left: 20%;
}

.wrapper_countries_Norway {
  position: absolute;
  top: 250px;
  left: 15%;
}
.wrapper_countries_Georgia {
  position: absolute;
  top: 191px;
  right: 20%;
}
.wrapper_countries_Hong-Kong {
  position: absolute;
  top: 250px;
  right: 15%;
}

@media (max-width: 611px) {
  .info_world-map {
    display: none;
  }
}
</style>
