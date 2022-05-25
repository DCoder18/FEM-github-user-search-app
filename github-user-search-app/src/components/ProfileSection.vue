<template>
  <section class="profile">
    <ProfileBasic />
    <ProfileStats />
  </section>
</template>


<script>
import ProfileBasic from './ProfileBasic.vue'
import ProfileStats from './ProfileStats.vue'

export default {
  name: 'App',
  components: {
    ProfileBasic,
    ProfileStats,
  }
}
</script>


<style lang="scss" scoped>
  .profile {
    display: grid;
    grid-template-columns: 13rem 2fr 1fr;
    background-color: var(--clr-off-white);
    border-radius: 1.5rem;
    padding: 4.8rem;
  }
</style>