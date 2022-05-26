<template>
  <img class="profile--img" src="" alt="Img">
  <div>
    <h2 class="profile--name">The Octocat</h2>
    <h3 class="profile--username">@octocat</h3>
  </div>
  <p class="profile--join-date">Joined 25 Jan 2011</p>
  <p class="profile--bio">
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt expedita iste officiis sapiente et ab voluptatibus.
  </p>
  
</template>


<style lang="scss" scoped>
  .profile {
    &--name {
      font-size: var(--fs-600);
      color: var(--clr-black-1);
      font-weight: 700;
    }

    &--username {
      font-size: var(--fs-300);
      color: var(--clr-bright-blue);
      font-weight: 400;
      margin-bottom: 2rem;

      @media (max-width:45em) {
        margin-bottom: 4px;
      }
    }

    &--join-date{
      font-size: var(--fs-200);
      color: var(--clr-grey-blue);
      grid-column: 3 / 4;

      @media (max-width:45em) {
        grid-column: 2 / span 2;
      }
    }

    &--bio {
      font-size: var(--fs-200);
      color: var(--clr-navy-blue);
      grid-column: 2 / 4;
      margin-bottom: 3rem;

      @media (max-width:45em) {
        grid-column: 1 / span 3;
        margin-top: 2.4rem;
      }
    }
  }
</style>