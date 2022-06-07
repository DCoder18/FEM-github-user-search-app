<template>
  <section class="profile" :class="{'dark-mode' : darkMode}">
    <ProfileBasic :darkMode="darkMode" :users="users" />
    <ProfileStats :darkMode="darkMode" :users="users" />
    <ProfileLinks :darkMode="darkMode" :users="users" />
  </section>
</template>


<script>
import ProfileBasic from './ProfileBasic.vue'
import ProfileStats from './ProfileStats.vue'
import ProfileLinks from './ProfileLinks.vue'

export default {
  name: 'App',
  components: {
    ProfileBasic,
    ProfileStats,
    ProfileLinks
  },

  props: {
    darkMode: Boolean,
    query: String,
  },

  data() {
    return {
      users: {},
    }
  },

  mounted() {
    fetch('https://api.github.com/users/mojombo')
    .then(res => res.json())
    .then(data => this.users = data)
    .catch(err => console.log(err.message))
  },
}
</script>


<style lang="scss" scoped>
  .profile {
    display: grid;
    grid-template-columns: 13rem 2fr 1fr;
    background-color: var(--clr-off-white);
    border-radius: 1.5rem;
    padding: 4.8rem;
    box-shadow: 0px 6px 20px -15px var(--box-shadow-blue);

    &.dark-mode {
      background-color: var(--clr-dark-blue);
      box-shadow: none;
    }

    @media (max-width:30em) {
      display: block;
    }
  }
</style>