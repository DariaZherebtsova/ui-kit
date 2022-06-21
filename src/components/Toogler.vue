<template>
  <label class="toggler toggler_has-icon">
    <input type="checkbox" class="toggler__input" id="theme-changer" />
    <div class="toggler__state">
      <SunTogglerIcon />
      <div class="toggler__control">
        <TogglerIcon />
      </div>
      <MoonTogglerIcon />
    </div>
  </label>
</template>

<script setup lang="ts">
import TogglerIcon from './icons/IconToggler.vue';
import SunTogglerIcon from './icons/IconTogglerSun.vue';
import MoonTogglerIcon from './icons/IconTogglerMoon.vue';
</script>

<style lang="scss">
.toggler {
  display: inline-flex;
  cursor: pointer;
  position: relative;

  &__input {
    position: absolute;
    outline: none;
    clip: rect(0, 0, 0, 0);
  }

  &__state {
    display: flex;
    align-items: center;
    gap: 12px;
  }

  &__control {
    border: 1px solid var(--grey-2);
    box-sizing: border-box;
    border-radius: 16px;
    box-sizing: border-box;
    width: 52px;
    height: 28px;
    display: flex;
    justify-content: start;
    align-items: center;
  }

  &__icon {
    fill: var(--grey-2);
  }

  &__title {
    font-family: Inter, sans-serif;
    font-style: normal;
    font-weight: 400;
    font-size: 16px;
    line-height: 24px;
    color: var(--grey-4);
  }

  &__input:checked ~ .toggler__state .toggler__control {
    justify-content: end;
    border: 2px solid var(--blue-1);
    background: var(--blue-1);
  }

  &__input:checked ~ .toggler__state .toggler__icon {
    fill: var(--white);
  }

  &__input:disabled ~ .toggler__state .toggler__control {
    background: var(--grey-2);
    border-color: var(--grey-2);
    cursor: not-allowed;
  }

  &__input:disabled ~ .toggler__state .toggler__title {
    cursor: not-allowed;
  }

  &__input:disabled ~ .toggler__state .toggler__icon {
    fill: var(--grey-3);
  }

  &__input:focus ~ .toggler__state .toggler__title {
    text-decoration: underline;
  }
}
</style>
