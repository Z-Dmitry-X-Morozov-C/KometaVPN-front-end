<script setup lang="ts">
import Comet from "../Comet.vue";
</script>

<template>
  <div class="title-conteiner-comet">
    <Comet class="title-conteiner-comet_comet-1"/>
    <Comet class="title-conteiner-comet_comet-2"/>
    <Comet class="title-conteiner-comet_comet-3"/>
  </div>
</template>

<style scoped>
 .title-conteiner-comet {
  display: flex;
  position: relative;
  gap: 100px;
  width: 50%;
  max-width: 100px;
  height: 600px;
} 

.title-conteiner-comet_comet-1 {
  position: relative;
  scale: 0.7;
  left: -10%;
  top: -12%;
  animation: stars-flow 1.5s ease-out forwards;
} 
.title-conteiner-comet_comet-2 {
  transform: rotate(45deg);
  position: relative;
  left: 20%;
  scale: 1.2;
  animation: stars-flow 3.5s ease-out forwards;
}

.title-conteiner-comet_comet-3 {
  position: relative;
  left: 10%;
  top: 10%;
  scale: 0.9;
  animation: stars-flow 2.5s ease-out forwards;
}  

@media (max-width: 847px) {
  .title-conteiner-comet_comet-1 {
    scale: 0.3;
    top: -5%;
    left: 60%;
  }

  .title-conteiner-comet_comet-2 {
    scale: 0.65;
    left: 0;
  }

  .title-conteiner-comet_comet-3 {
    scale: 0.4;
    top: 5%;
    left: -80%;
  }
}

@keyframes stars-flow {
  0% {
    transform: translatex(-10%) translatey(0);
    rotate: 45deg;
    opacity: 0;
  }

  50% {
    opacity: 1;
  }

  100% {
    transform: translatex(0) translatey(-10%);
    rotate: 45deg;
  }
}
</style>
