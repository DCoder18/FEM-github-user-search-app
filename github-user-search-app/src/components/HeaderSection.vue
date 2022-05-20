<template>
  <header>
    <div class="container">
      <div class="header">
        <h1>devfinder</h1>
        <div class="color-switch">
          <span class="color-switch__title">Dark</span>
          <img class="color-switch__icon" src="../assets/images/icon-moon.svg" alt="">
        </div>
      </div>
    </div>
  </header>
</template>


<style lang="scss" scoped>
  .header {
    display: flex;
    justify-content: space-between;
    width: 100%;
  }
  h1 {
    color: var(--clr-black-3);
    font-size: var(--ff-500);
  }

  .color-switch {
    display: flex;
    align-content: center;
    justify-content: center;
    position: relative;

    &__title {
      text-transform: uppercase;
      color: var(--clr-grey-blue);
      font-weight: 700;
      font-size: var(--ff-100);
    }

    &__icon {
      width: 2rem;
      height: 2rem;
      position: absolute;
      left: 4.5rem;
      bottom: 2rem;
    }
  }
</style>