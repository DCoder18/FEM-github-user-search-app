<template>
 <div class="links">
  <div class="links__item">
    <span><img class="links__icon links__icon--location" src="../assets/images/icon-location.svg" alt=""></span>
    <span><p class="links--location">San Francisco</p></span>
  </div>

  <div class="links__item">
    <span><img class="links__icon links__icon--twitter" src="../assets/images/icon-twitter.svg" alt=""></span>
    <span><p class="links--twitter">@octocat</p></span>
  </div>

  <div class="links__item">
    <span><img class="links__icon links__icon--website" src="../assets/images/icon-website.svg" alt=""></span>
    <span><p class="links--website">https://github.blog</p></span>
  </div>

   <div class="links__item">
    <span><img class="links__icon links__icon--company" src="../assets/images/icon-company.svg" alt=""></span>
    <span><p class="links--company">@github</p></span>
  </div>
 </div>
</template>


<style lang="scss" scoped>
  .links {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-column: 2 / 4;
    grid-gap: 2rem 10rem;
    margin-top: 30px;

    @media (max-width:45em) {
      grid-column: 1 / span 3;
      grid-gap: 2.5rem;
    }

    @media (max-width:30em) {
      display: block;
    }

    &__item {
      display: flex;
      align-items: center;
      
      @media (max-width:30em) {
        margin-bottom: 1.6rem;
      } 
    }

    &__icon {
      margin-right: 2rem;
      
      &--location {
        width: 1.4rem;
        height: 2rem;
      }

      &--twitter {
        width: 2rem;
        height: 1.6rem;
      }

      &--website {
        width: 1.7rem;
        height: 1.7rem;
      }

       &--company {
        width: 2rem;
        height: 2rem;
      }
    }

    p {
      font-size: var(--fs-200);
      color: var(--clr-navy-blue);

      &.dark-mode {
        color: var(--white);
      }
    }
  }
</style>