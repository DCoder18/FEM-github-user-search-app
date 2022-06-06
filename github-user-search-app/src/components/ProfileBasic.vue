<template>
  <img class="profile--img" :src=users.avatar_url alt="Img">
  <div>
    <h2 class="profile--name" :class="{'dark-mode' : darkMode}">{{ users.name }}</h2>
    <h3 class="profile--username">{{ users.login }}</h3>
  </div>
  <p class="profile--join-date" :class="{'dark-mode' : darkMode}">{{ users.created_at }}</p>
  <p class="profile--bio" :class="{'dark-mode' : darkMode}">
    {{ users.bio }}
  </p>
</template>

<script>
  export default {
    props: {
      darkMode: Boolean,
      users: Object,
    },
  }
</script>

<style lang="scss" scoped>
  .profile {
    &--name {
      font-size: var(--fs-600);
      color: var(--clr-black-1);
      font-weight: 700;

      &.dark-mode {
        color: var(--clr-white);
      }
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

      &.dark-mode {
        color: var(--clr-white);
      }

      @media (max-width:45em) {
        grid-column: 2 / span 2;
      }
    }

    &--bio {
      font-size: var(--fs-200);
      color: var(--clr-navy-blue);
      grid-column: 2 / 4;
      margin-bottom: 3rem;

      &.dark-mode {
        color: var(--clr-white);
      }

      @media (max-width:45em) {
        grid-column: 1 / span 3;
        margin-top: 2.4rem;
      }
    }
  }
</style>