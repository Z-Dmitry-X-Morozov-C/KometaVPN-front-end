<template>
  <div>
    <NuxtLayout />
    <NuxtPage />
  </div>
</template>

<script setup>
import "~/assets/styles.css";

useHead({
  title: "KometaVPN",
  meta: [{ name: "description", content: "My amazing site." }],
  meta: [{property: "og:image", content: "~/assets/img/WebPreview.jpg"}],
  bodyAttrs: {
    class: "test",
  },
  script: [{ innerHTML: "console.log('Hello world')" }],
});
</script>
