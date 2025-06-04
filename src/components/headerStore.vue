<template>
  <header class="header">
    <div class="header__container">
      <div class="header__logo">MyShop</div>

      <button class="header__burger" @click="toggleMenu">☰</button>

      <nav :class="['header__nav', { 'header__nav--open': menuOpen }]">
        <a href="#" class="header__link">Home</a>
        <a href="#" class="header__link">Products</a>
        <a href="#" class="header__link">Contact</a>
      </nav>

      <div class="header__cart">🛒 <span class="header__cart-count">3</span></div>
    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue'
const menuOpen = ref(false)
const toggleMenu = () => {
  menuOpen.value = !menuOpen.value
}
</script>

<style scoped lang="scss">
.header {
  background-color: #222;
  color: white;
  padding: 1rem 2rem;

  &__container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: relative;
  }

  &__logo {
    font-size: 1.5rem;
    font-weight: bold;
  }

  &__burger {
    display: none;
    font-size: 1.5rem;
    background: none;
    border: none;
    color: white;
    cursor: pointer;
  }

  &__nav {
    display: flex;
    gap: 1.5rem;

    &--open {
      display: flex;
      flex-direction: column;
      position: absolute;
      top: 100%;
      left: 0;
      right: 0;
      background-color: #222;
      padding: 1rem;
      z-index: 100;
    }
  }

  &__link {
    color: white;
    text-decoration: none;
    font-weight: 500;

    &:hover {
      text-decoration: underline;
    }
  }

  &__cart {
    position: relative;
    font-size: 1.2rem;
  }

  &__cart-count {
    position: absolute;
    top: -8px;
    right: -10px;
    background: red;
    color: white;
    border-radius: 50%;
    padding: 2px 6px;
    font-size: 0.75rem;
  }

  // Адаптив
  @media (max-width: 768px) {
    &__burger {
      display: block;
    }

    &__nav {
      display: none;
      flex-direction: column;
      align-items: flex-start;
      gap: 1rem;
    }

    &__cart {
      margin-left: 1rem;
    }
  }
}
</style>
