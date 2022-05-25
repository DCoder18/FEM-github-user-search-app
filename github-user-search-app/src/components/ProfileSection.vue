<template>
  <section class="profile">
    <ProfileBasic> </ProfileBasic>
  </section>
</template>


<script>
import ProfileBasic from './ProfileBasic.vue'

export default {
  name: 'App',
  components: {
    ProfileBasic,
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