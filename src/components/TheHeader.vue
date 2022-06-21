<template>
  <header class="header">
    <div class="container">
      <div class="header__top-menu">
        <div class="logo">
          <svg
            class="logo__icon"
            width="110"
            height="32"
            viewBox="0 0 110 32"
            xmlns="http://www.w3.org/2000/svg"
          >
            <rect y="1" width="30" height="30" />
            <rect x="38" width="32" height="32" rx="16" />
            <path d="M78 0L110 32H78V0Z" />
          </svg>
        </div>

        <div class="header__links-group">
          <a class="header__link" href="">Components</a>
          <a class="header__link" href="">About</a>
          <a class="header__link" href="">Contact</a>

          <Toogler />
        </div>
      </div>
      <h1 class="header__title">Reusable component library</h1>
    </div>
  </header>
</template>

<script setup lang="ts">
import Toogler from './Toogler.vue';
</script>

<style lang="scss">
.header {
  background-color: var(--main-bg);

  &__top-menu {
    padding: 16px 0;
    display: flex;
    justify-content: center;

    @media screen and (min-width: 600px) {
      justify-content: space-between;
    }
  }

  &__links-group {
    display: none;

    @media screen and (min-width: 600px) {
      display: flex;
      align-items: center;
      gap: 24px;
    }
  }

  &__link {
    @media screen and (min-width: 600px) {
      text-decoration: none;
      font-family: Inter, sans-serif;
      font-style: normal;
      font-weight: 400;
      font-size: 16px;
      line-height: 24px;
      color: var(--font-color);
    }
  }

  &__title {
    margin: 49px 16px 69px;
    font-family: Inter, sans-serif;
    font-style: normal;
    font-weight: 400;
    font-size: 28px;
    line-height: 38px;
    color: var(--grey-4);

    @media screen and (min-width: 600px) {
      margin: 38px 0 40px;
      font-family: Inter, sans-serif;
      font-style: normal;
      font-weight: 500;
      font-size: 50px;
      line-height: 64px;
      color: var(--font-color);
    }
  }
}
</style>
