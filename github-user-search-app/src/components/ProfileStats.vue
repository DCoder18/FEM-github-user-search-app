<template>
 <div class="stats">
  <div class="stats__item">
    <h4>Repos</h4>
    <p class="stats--repos">8</p>
  </div>

  <div class="stats__item">
    <h4>Followers</h4>
    <p class="stats--followers">3898</p>
  </div>

  <div class="stats__item">
    <h4>Following</h4>
    <p class="stats--following">9</p>
  </div>
 </div>
</template>


<style lang="scss" scoped>
  .stats {
    background-color: var(--clr-grey);
    border-radius: 1rem;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-column: 2 / 4; 
    grid-gap: 10rem;
    padding: 1.5rem 3rem;

    @media (max-width:45em) {
      grid-column: 1 / span 3;
      grid-gap: 2rem;
    }

    @media (max-width:30em) {
      grid-gap: 2rem;
    }
    
    &__item {
      h4 {
        font-size: var(--fs-100);
        color: var(--clr-navy-blue);
        font-weight: 400;

        &.dark-mode {
          color: var(--white);
        }
      }

      p {
        font-size: var(--fs-500);
        color: var(--clr-black-1);
        font-weight: 700;

        &.dark-mode {
          color: var(--white);
        }
      }
    }
  }
</style>