<template>
  <section class="info_VLESS justify-center">
    <div>
      <p class="title">VLESS</p>
    </div>
    <div>
      <p class="text">Протокол что обходит даже великую китайскую стену</p>
    </div>
    <div class="info_VLESS_earth">
      <img src="/assets/img/Earth.svg" alt="Earth" class="earth" />
    </div>
    <div class="gradient-anim"></div>
  </section>
</template>

<script></script>

<style scoped>
.info_VLESS {
  gap: 23px;
  position: relative;
  width: 100%;
}

.gradient-anim {
  height: 100%;
  width: 100%;
  position: absolute;
  bottom: 0;
  background: linear-gradient(180deg, rgba(0, 0, 0, 0) 60%, #d400ffb0);
  animation: flow-light 10s cubic-bezier(0.8, 0.2, 1, 1) infinite reverse;
}

.info_VLESS_earth {
  margin-top: 3vw;
  max-width: 100%;
  height: auto;
}

.earth {
  max-width: 100%;
  height: auto;
}

@keyframes flow-light {
  0%,
  100% {
    opacity: 0;
  }

  50% {
    opacity: 1;
  }
}

@media (max-width: 422px) {
  .justify-center {
    align-items: start;
  }

  .title {
    text-align: start;
    padding: 5px;
  }
  .text {
    text-align: start;
    padding: 5px;
  }
}
</style>
