<template>
  <div class="empty-search">
    <p>Such empty. Search a github user to see their information!</p>
  </div>
</template>

<script>
  export default {
    props: {
      darkMode: Boolean,
      userExists: Boolean
    },

    data() {
      return {
        query: ''
      }
    },

    methods: {
      updateQuery() {
        console.log(this.users);
      }
    }
  }
</script>

<style lang="scss" scoped>
 .empty-search {
    background-color: var(--clr-off-white);
    border-radius: 1.5rem;
    padding: 4.8rem;
    box-shadow: 0px 6px 20px -15px var(--box-shadow-blue);
    font-size: var(--fs-300);
    color: var(--clr-black-1);
    font-weight: 700;
    text-align: center;

     &.dark-mode {
      background-color: var(--clr-dark-blue);
      color: var(--clr-white);
      box-shadow: none;
    }

    p {
      opacity: 60%;
    }
 }
</style>