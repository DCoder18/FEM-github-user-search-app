<template>
  <section class="search">
    <form action="#" method="post">
      <div class="searchbar">
        <input type="search" name="" id="" placeholder="Search GitHub username...">
        <img class="icon icon--search" src="../assets/images/icon-search.svg" alt="">
        <button class="btn-search">Search</button>
      </div>
    </form>
  </section>
</template>


<style lang="scss" scoped>
  .searchbar {
    position: relative;
    margin-bottom: 2.4rem;
  }

  input {
    width: 100%;
    height: 7rem;
    border: none;
    outline: none;
    border-radius: 1.5rem;
    box-shadow: 0px 6px 20px -15px var(--box-shadow-blue);
    font-size: var(--fs-400);
    font-family: inherit;
    padding-left: 8rem;
    background-color: var(--clr-off-white);

    @media (max-width:30em) {
      padding-left: 6rem;
    }
  }

  .icon {
    &--search {
      width: 2.4rem;
      height: 2.4rem;
      position: absolute;
      top: 2.2rem;
      left: 2.2rem;
    }
  }

  .btn-search {
    border: none;
    background-color: var(--clr-bright-blue);
    color: var(--clr-white);
    border-radius: 1rem;
    width: 10rem;
    height: 5rem;
    font-family: inherit;
    font-size: var(--fs-300);
    position: absolute;
    right: 1rem;
    top: 1rem
  }
</style>