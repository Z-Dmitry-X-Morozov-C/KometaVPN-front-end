<template>
  <div>
    <NuxtLayout />
    <NuxtPage />
  </div>
</template>

<script setup>
import "~/assets/styles.css";

useSeoMeta({
  title: "KometaVPN",
  ogTitle: 'Заголовок',
  ogDescription: 'Описание',
  ogImage: '~/assets/img/WebPreview.jpg',
});
</script>
