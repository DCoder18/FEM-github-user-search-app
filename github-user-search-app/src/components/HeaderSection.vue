<template>
  <section class="header">
    <h1 :class="{'dark-mode' : darkMode}">devfinder</h1>
    <div class="color-switch" @click="modeToggle">
      <span :class="{'dark-mode' : darkMode}" class="color-switch__title">{{ darkMode ? 'Light' : 'Dark' }}</span>
      <img v-if="darkMode" class="color-switch__icon" src="../assets/images/icon-sun.svg" alt="">
      <img v-else class="color-switch__icon" src="../assets/images/icon-moon.svg" alt="">
    </div>
  </section>
</template>

<script>
export default {
  props: {
    darkMode: Boolean
  },
  methods: {
    modeToggle() {
      this.$parent.modeToggle();
    },
  },
}
</script>

<style lang="scss" scoped>
  .header {
    display: flex;
    justify-content: space-between;
    width: 100%;
    margin-bottom: 3.6rem;
  }
  
  h1 {
    color: var(--clr-black-3);
    font-size: var(--fs-600);

    &.dark-mode {
      color: var(--clr-white);
    }
  }

  .color-switch {
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    cursor: pointer;

    &__title {
      text-transform: uppercase;
      color: var(--clr-grey-blue);
      font-weight: 700;
      font-size: var(--fs-100);
      margin-right: 1.6rem;
      letter-spacing: 2.4px;

      &.dark-mode {
        color: var(--clr-white);
      }
    }

    &__icon {
      width: 2rem;
      height: 2rem;
    }
  }
</style>
