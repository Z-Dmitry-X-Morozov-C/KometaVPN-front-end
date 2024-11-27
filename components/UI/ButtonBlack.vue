<template>
  <button>
    <a :href="link" target="_blank">
      {{ text }}
    </a>
  </button>
</template>

<script setup>
import { defineProps } from "vue";

const props = defineProps({
  text: {
    type: String,
    required: true,
  },

  link: {
    type: String,
    required: true,
  },
});
</script>

<style scoped>
button {
  display: flex;
  font-size: calc(18px + (6 + 6 * 0.7) * ((100vw - 320px) / 1920));
  justify-content: center;
  align-items: center;
  padding: 1em;
  border-radius: 42px;
  border: none;
  border: 1px solid white;
  background-color: transparent;
  cursor: pointer;
}
a {
  text-decoration: none;
  color: rgb(255, 242, 242);
}

@media (max-width: 847px) {
  button {
    padding: 0.8em;
  }
}

@media (max-width: 422px) {
  button {
    padding: 0.5em;
  }
}
</style>
