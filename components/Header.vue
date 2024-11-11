<template>
  <div class="header">
    <div class="header-content">
      <div class="header-content_logo">
        <img src="/assets/img/Frame 5.svg" alt="KametaLOGO" />
      </div>
    </div>
    <div class="header-content-nav">
      <div class="cursor header-content-nav_proj-point">Цель проекта</div>
      <div class="cursor header-content-nav_contact-us">Связаться с нами</div>
    </div>
  </div>
</template>

<script setup></script>

<style scoped>
.header {
  position: sticky;
  top: 10px;
  margin: 40px 12px;
  height: 64px;
  border-radius: 118px;
  backdrop-filter: blur(5px);
  background: rgba(37, 37, 37, 0.4);
  border: 1px solid rgb(47, 47, 47);
  padding: 12px 24px;
  display: flex;
  align-items: center;
  justify-content: space-between;
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
</style>
