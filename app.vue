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
  ogUrl: "KometaVPN",
  ogTitle: "KometaVPN — Быстрый и Надежный Доступ к Сети",
  ogDescription:
    "Мы используем передовую технологию A.T.H.E.N.A для оптимизации маршрутов, повышения стабильности соединения и защиты данных, обеспечивая удобный и безопасный доступ к интернет-ресурсам",
  ogImage: "~/assets/img/WebPreview.jpg",
});
</script>
