<template>
  <div>
    <GridBackgr />
    <!-- дубликация хедера, для проверки поведения хедера, потом удалить этот ужас-->
    <Header v-for="item in 10"></Header>
  </div>
</template>

<script setup></script>

<style scoped></style>
