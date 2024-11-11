<template>
  <div class="grid-section">
    <div v-for="item in 133" class="grid-section_conteiner"></div>
  </div>
</template>

<script></script>

<style scoped>
.grid-section {
  position: absolute;
  width: 100%;
  top: 0;
  z-index: -10;
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(128px, 1fr));
  grid-template-rows: repeat(7, 128px);
  height: 695px;
  overflow: hidden;
}

.grid-section_conteiner {
  position: relative;
  border: 1px solid rgba(116, 116, 116, 0.05);
}

.grid-section_conteiner::before {
  content: "";
  height: 10px;
  width: 10px;
  background-color: rgba(116, 116, 116, 0.05);
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  border-radius: 50%;
}

</style>
