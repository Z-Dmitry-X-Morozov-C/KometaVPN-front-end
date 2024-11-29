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
  ogUrl: "KometaVPN.ru",
  ogTitle: "KometaVPN — Быстрый и Надежный Доступ к Сети",
  ogDescription:
    "Мы используем передовую технологию A.T.H.E.N.A для оптимизации маршрутов, повышения стабильности соединения и защиты данных, обеспечивая удобный и безопасный доступ к интернет-ресурсам",
  ogImage: "https://drive.google.com/file/d/1_s2bJCQ-cCcy1KLz16bHbxCBGCPj9yC1/view?usp=sharing",
});
</script>
