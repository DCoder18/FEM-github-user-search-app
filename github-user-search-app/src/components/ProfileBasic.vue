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
      font-size: var(--ff-600);
      color: var(--clr-black-1);
      font-weight: 700;
    }

    &--username {
      font-size: var(--ff-300);
      color: var(--clr-bright-blue);
      font-weight: 400;
      margin-bottom: 2rem;
    }

    &--join-date{
      font-size: var(--ff-200);
      color: var(--clr-grey-blue);
      grid-column: 3 / 4;
    }

    &--bio {
      font-size: var(--ff-200);
      color: var(--clr-navy-blue);
      grid-column: 2 / 4;
    }
  }
</style>