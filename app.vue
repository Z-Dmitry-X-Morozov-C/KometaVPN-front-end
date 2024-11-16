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
  ogImage: '~/assets/img/WebPreview.jpg',
});
</script>
