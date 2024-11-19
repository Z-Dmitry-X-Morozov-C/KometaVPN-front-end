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
  ogImage: 'https://sun9-29.userapi.com/impg/UnoNNeF2VHHhWBAmfiqJ9PqVi3EQH97RvsVBoQ/_e7dyEeMkYk.jpg?size=1280x666&quality=95&sign=eff85ffb42c2cb8ce828daec84a3f8fd&type=album',
});
</script>
