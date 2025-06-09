<script setup>
//import { RouterLink, RouterView } from 'vue-router'
//import HelloWorld from './components/HelloWorld.vue'
import HeaderStore from './components/headerStore.vue'
import MainStore from './components/mainStore.vue'
</script>

<template>
  <HeaderStore />
  <MainStore />

  <RouterView />
</template>

<style scoped></style>
