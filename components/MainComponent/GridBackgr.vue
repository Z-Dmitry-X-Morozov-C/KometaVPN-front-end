<template>
  <div class="flex">
    <div class="grid-section">
      <div v-for="item in 200" class="grid-section_conteiner"></div>
    </div>

  </div>
</template>

<script></script>

<style scoped>
.flex {
  display: flex;
}

.grid-section {
  display: grid;
  grid-template-columns: repeat(20, 128px);
  grid-template-rows: repeat(4, 128px);
  position: absolute;
  width: 110%;
  height: 495px;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
  overflow: hidden;
}

.grid-section_conteiner {
  position: relative;
  border: 1px solid  rgba(116, 116, 116, 0.05);
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
