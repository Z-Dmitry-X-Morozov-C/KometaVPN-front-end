<template>
  <div>
    <div class="main-wrapper">
      <div>
        <p class="main-wrapper_title">
          Быстрый <br />
          Приватный <br />
          Свободный
        </p>
      </div>
      <button class="main-wrapper_btn main-wrapper_btn-text">Попробовать сейчас</button>
    </div>
  </div>
  <div class="main-wrapper_stars"><img src="/assets/img/titleStars.svg" alt="titleStars" /></div>
</template>

<script setup></script>

<style scoped>
@keyframes stars-flow {
  from {
    transform: translatex(0) translatey(2%);
    opacity: 0;
  }
  to {
    transform: translatex(2%) translatey(0);
    opacity: 1;
  }
}
.main-wrapper {
  position: absolute;
  left: 8dvw;
  z-index: 1;
}

.main-wrapper_title {
  font-family: SF Pro Display;
  font-style: italic;
  font-size: calc(34px + 99 * (100vw / 1920));
  font-weight: 900;
  line-height: 85%;
  cursor: default;
}

.main-wrapper_stars {
  scale: 1.3;
  position: absolute;
  right: 6vw;
  top: 23%;
  animation: stars-flow 2s ease-out forwards;
}

.main-wrapper_stars > img {
  width: 50vw;
  height: auto;
}

.main-wrapper_btn {
  color: black;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding: 2.6%;
  border-radius: 12px;
  border: none;
  background: rgb(255, 255, 255);
  margin-top: 6vw;
  cursor: pointer;
}

.main-wrapper_btn-text {
  font-size: calc(18px + 6 * (100vw / 1920));
}

@media (max-width: 847px) {
  @keyframes stars-flow {
    from {
      transform: translatex(-2%) translatey(0);
      opacity: 0;
    }
    to {
      transform: translatex(0) translatey(-2%);
      opacity: 1;
    }
  }

  .main-title_text {
    font-size: calc(34px + (99 + 99 * 0.7) * ((100vw - 375px) / 1920));
  }

  .main-wrapper {
    position: relative;
  }

  .main-wrapper_stars {
    scale: 3;
    position: static;
    margin: 40% 0 0 25%;
  }

  .main-wrapper_btn-text {
    font-size: calc(18px + (6 + 6 * 0.7) * ((100vw - 375px) / 1920));
  }
}
</style>
