<template>
  <section>
    <div class="info_athena justify-center">
      <div class="info_athena-title justify-center">
        <p class="title title-1">Собственная технология</p>
        <p class="title">A.T.H.E.N.A</p>
      </div>
      <div>
        <p class="info_athena-text text">
          Нейросеть для оптимизации трафика, выбора маршрутов <br />и создания цепочек прокси
        </p>
      </div>
    </div>
    <div class="info_athena_animation">
      <div class="info_athena_background"></div>
      <div class="justify-center">
        <img class="info_athena-wave" src="/assets/img/Wave.svg" alt="ground" />
      </div>
      <div class="info_athena_beam"></div>
      <div class="info_athena_debris">
        <div class="info_athena_piece piece-1 piece-form-1"></div>
        <div class="info_athena_piece piece-2 piece-form-2"></div>
        <div class="info_athena_piece piece-3 piece-form-1"></div>
        <div class="info_athena_piece piece-4 piece-form-1"></div>
        <div class="info_athena_piece piece-5 piece-form-2"></div>
        <div class="info_athena_piece piece-6 piece-form-1"></div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.title {
  font-style: normal;
}

.title-1 {
  font-size: calc(18px + (14 + 14 * 0.7) * ((100vw - 320px) / 1920));
  font-weight: 500;
}

.info_athena {
  margin: 0 auto;
  position: relative;
  gap: 40px;
}

.info_athena-title {
  gap: 10px;
}

.info_athena_animation {
  position: relative;
  margin-top: 28px;
  overflow: hidden;
  height: 740px;
}

.info_athena-wave {
  position: absolute;
  bottom: 0;
  width: 2000px;
  height: auto;
}

.info_athena_beam {
  position: absolute;
  height: 100%;
  width: 22px;
  left: 50%;
  top: -20px;
  transform: translateX(-50%);
  background: linear-gradient(0deg, rgb(255, 0, 215) 60%, #050505 99%);
  filter: blur(5px);
  z-index: -1;
}

.info_athena_background {
  position: absolute;
  top: -10px;
  height: 100%;
  width: 100%;
  background: linear-gradient(0, rgba(255, 0, 215, 0.3) 70%, #050505 99%);
  z-index: -10;
}

.info_athena_debris {
  position: relative;
  justify-self: center;
}

.info_athena_piece {
  position: absolute;
  background-color: black;
}

.piece-form-1 {
  clip-path: polygon(51% 5%, 69% 52%, 43% 100%, 12% 75%, 18% 34%);
  height: 50px;
  width: 50px;
}
.piece-form-2 {
  clip-path: polygon(37% 7%, 63% 54%, 43% 98%, 5% 64%, 9% 33%);
  height: 100px;
  width: 100px;
}

.piece-1 {
  right: 43px;
  top: 63px;
  animation: piece-flow-2 2s ease-in infinite;
}

.piece-2 {
  right: 120px;
  top: 97px;
  animation: piece-flow-1 4s ease-in-out infinite;
}

.piece-3 {
  right: 50px;
  top: 230px;
  animation: piece-flow-1 2s ease-out infinite;
}

.piece-4 {
  left: 43px;
  top: 38px;
  animation: piece-flow-2 2s ease-in infinite;
}

.piece-5 {
  left: 140px;
  top: 91px;
  animation: piece-flow-2 4s ease-in-out infinite;
}

.piece-6 {
  left: 60px;
  top: 200px;
  animation: piece-flow-2 2s ease-in infinite;
}

@keyframes piece-flow-1 {
  0%,
  100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(10px);
  }
}
@keyframes piece-flow-2 {
  0%,
  100% {
    transform: translateY(10px);
  }
  50% {
    transform: translateY(0);
  }
}
</style>
