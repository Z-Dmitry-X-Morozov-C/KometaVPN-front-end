<template>
  <header class="header">
    <div class="header-content">
      <div>
        <img class="header-content_logo" src="/assets/img/LOGO.svg" alt="KametaLOGO" />
      </div>
    </div>
    <div class="header-content-nav">
      <div @click.prevent="smoothScroll('#Point')" class="cursor header-content-nav_proj-point">Цель проекта</div>
      <NuxtLink to="about">
        <div class="cursor header-content-nav_contact-us">Политика конфиденциальности</div>
      </NuxtLink>
    </div>
  </header>
</template>

<script setup>
import { useWindowScroll } from "@vueuse/core";

const smoothScroll = (target) => {
  const { x, y } = useWindowScroll({ behavior: "smooth" });
  y.value = 900;
};
</script>

<style scoped>
.header {
  position: sticky;
  top: 10px;
  margin: 40px auto;
  width: 90%;
  height: 64px;
  border-radius: 118px;
  backdrop-filter: blur(60px);
  background: rgba(37, 37, 37, 0.4);
  border: 1px solid rgb(47, 47, 47);
  padding: 12px 24px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  z-index: 1000;
}

.header-content_logo {
  width: 100%;
  height: 100%;
}

.header-content-nav {
  display: flex;
  align-items: center;
  font-size: 24px;
  gap: 1em;
}

.cursor {
  cursor: pointer;
}

a {
  font-style: none;
}

@media (max-width: 847px) {
  .header {
    justify-content: center;
  }

  .header-content-nav {
    display: none;
  }
}
</style>
