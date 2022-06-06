<template>
 <div class="stats" :class="{'dark-mode' : darkMode}">
  <div class="stats__item">
    <h4 :class="{'dark-mode' : darkMode}">Repos</h4>
    <p class="stats--repos" :class="{'dark-mode' : darkMode}">{{ users.public_repos }}</p>
  </div>

  <div class="stats__item">
    <h4 :class="{'dark-mode' : darkMode}">Followers</h4>
    <p class="stats--followers" :class="{'dark-mode' : darkMode}">{{ users.followers }}</p>
  </div>

  <div class="stats__item">
    <h4 :class="{'dark-mode' : darkMode}">Following</h4>
    <p class="stats--following" :class="{'dark-mode' : darkMode}">{{ users.following }}</p>
  </div>
 </div>
</template>

<script>
  export default {
    props: {
      darkMode: Boolean,
      users: Object,
    }
  }
</script>


<style lang="scss" scoped>
  .stats {
    background-color: var(--clr-grey);
    border-radius: 1rem;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-column: 2 / 4; 
    grid-gap: 10rem;
    padding: 1.5rem 3rem;

    &.dark-mode {
      background-color: var(--clr-black-2);
    }

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
          color: var(--clr-white);
        }
      }

      p {
        font-size: var(--fs-500);
        color: var(--clr-black-1);
        font-weight: 700;

        &.dark-mode {
          color: var(--clr-white);
        }
      }
    }
  }
</style>