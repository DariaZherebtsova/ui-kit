<template lang="">
  <div class="card">
    <div class="card__content">
      <slot></slot>
    </div>
    <div class="card__caption">Modal dialog</div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.card {
  width: 164px;
  min-height: 210px;
  box-sizing: border-box;
  background: var(--main-bg);
  box-shadow: 0px 2px 4px var(--grey-alpha);
  border-radius: 8px;
  display: flex;
  flex-direction: column;
  align-items: center;

  @media screen and (min-width: 600px) {
    padding: 32px 24px;
    width: 350px;
    min-height: 367px;
    border-radius: 12px;
  }

  &__content {
    align-self: stretch;
    display: flex;
    flex-direction: column;
    justify-content: center;
    flex-grow: 1;
  }

  &__caption {
    padding: 10px 0;
    width: 100%;
    border-top: 1px solid var(--grey-2);
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    font-family: Inter, sans-serif;
    font-style: normal;
    font-weight: 400;
    font-size: 16px;
    line-height: 24px;
    color: var(--black);

    @media screen and (min-width: 600px) {
      font-family: Roboto, sans-serif;
      font-style: normal;
      font-weight: 500;
      font-size: 21px;
      line-height: 25px;
      color: var(--font-color);
      border: none;
    }
  }
}
</style>
