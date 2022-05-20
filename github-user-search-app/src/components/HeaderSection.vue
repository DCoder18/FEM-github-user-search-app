<template>
  <header>
    <div class="container">
      <div class="header">
        <h1>devfinder</h1>
        <div class="color-switch">
          <span class="color-switch__title">Dark</span>
          <img class="icon" src="../assets/images/icon-moon.svg" alt="">
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
    margin-bottom: 3.6rem;
  }
  h1 {
    color: var(--clr-black-3);
    font-size: var(--ff-600);
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
      margin-right: 1.6rem;
      letter-spacing: 2.4px;
    }
  }
</style>