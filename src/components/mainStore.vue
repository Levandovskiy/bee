<template>
  <div class="img__main">
    <img class="img__header" src="../assets/img/header/фон.png" alt="" />
  </div>
</template>
<script setup></script>
<style scoped lang="scss">
.img__main {
  display: flex;
  align-items: center;
  justify-content: center;
  // або потрібна висота
}

.img__header {
  max-width: 100%;
  height: auto;
}
</style>
