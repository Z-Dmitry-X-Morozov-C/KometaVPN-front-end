<template>
  <div class="comet">
    <div class="comet_trail"></div>
    <div>
      <img class="comet_img" src="/assets/img/COMET.svg" alt="COMET" />
    </div>
  </div>
</template>

<script setup></script>

<style scoped>
.comet {
    position: relative;
}

.comet_trail {
  height: 100%;
  width: 8px;
  background: linear-gradient(
    360deg,
    rgb(5, 5, 5) 10%,
    #38FA59, 50%,
    rgb(249, 249, 255) 90%
  );
}

.comet_img {
  position: absolute;
  transform: rotate(45deg);
  top: -33px;
  left: -32px;
  filter: drop-shadow(0 0 40px white);
  scale: 0.9;
}
</style>
