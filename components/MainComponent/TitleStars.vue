<template>
  <div class="title-conteiner-comet">
    <div class="title-conteiner-comet_comet-1">
      <div class="trail"></div>
      <div>
        <img class="title-conteiner-comet_img" src="/assets/img/COMET.svg" alt="COMET" />
      </div>
    </div>
    <div class="title-conteiner-comet_comet-2">
      <div class="trail"></div>
      <div>
        <img class="title-conteiner-comet_img" src="/assets/img/COMET.svg" alt="COMET" />
      </div>
    </div>
    <div class="title-conteiner-comet_comet-3">
      <div class="trail"></div>
      <div class="title-conteiner-comet_gradient">
        <img class="title-conteiner-comet_img" src="/assets/img/COMET.svg" alt="COMET" />
      </div>
    </div>
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

.trail {
  position: relative;
  height: 100%;
  width: 8px;
  background: linear-gradient(
    360deg,
    rgb(5, 5, 5) 20%,
    rgb(255, 0, 0) 40%,
    rgb(240, 111, 111) 50%,
    rgb(241, 241, 241) 70%,
    rgb(249, 249, 255) 100%
  );
}

.title-conteiner-comet_comet-1 {
  transform: rotate(45deg);
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

.title-conteiner-comet_img {
  position: absolute;
  transform: rotate(45deg);
  top: -8%;
  left: -400%;
  scale: 0.85;
  filter: drop-shadow(0 0 40px white);
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
