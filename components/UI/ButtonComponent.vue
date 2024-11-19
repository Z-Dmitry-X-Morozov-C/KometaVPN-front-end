<template>
  <button>
    {{ text }}
  </button>
</template>

<script setup>
import { defineProps } from "vue";

const props = defineProps({
  text: {
    type: String,
    required: true,
  },
});
</script>

<style scoped>
button {
  position: relative;
  display: flex;
  margin-top: 4.6vw;
  font-size: calc(18px + 6 * (100vw / 1920));
  color: black;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding: 20px;
  border-radius: 12px;
  border: none;
  background: rgb(255, 255, 255);
  cursor: pointer;
}
</style>
