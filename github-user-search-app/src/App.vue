<template>
  <div id="app">
    <div class="container">
      <header>
        <HeaderSection :darkMode="darkMode" />
      </header>
      <main>
        <SearchBar @update-query="updateQuery($event)" :darkMode="darkMode" :usersExists="userExists" :users="users"/>
        <ProfileSection :darkMode="darkMode" :users="users" />
      </main>
    </div>
  </div>
</template>

<script>
import HeaderSection from './components/HeaderSection.vue'
import SearchBar from './components/SearchBar.vue'
import ProfileSection from './components/ProfileSection.vue'

export default {
  name: 'App',
  components: {
    HeaderSection,
    SearchBar,
    ProfileSection,
  },

  data() {
    return {
      darkMode: false,
      users: {},
      query: 'mojombo',
      userExists: false,
    }
  },

  mounted() {
    this.updateQuery(this.query)
  },

  methods: {
    dark() {
      document.querySelector('body').classList.add('dark-mode')
      this.darkMode = true
    },

    light() {
      document.querySelector('body').classList.remove('dark-mode')
      this.darkMode = false
    },

    modeToggle() {
      if(this.darkMode || document.querySelector('body').classList.contains('dark-mode')) {
          this.light()
      } else {
          this.dark()
      }
    },

    updateQuery(query) {
      const url = 'https://api.github.com/users/'
      let updatedURL = `${url}${query}`

      fetch(updatedURL)
        .then(res => res.json())
        .then(data => this.users = data)
        .catch(err => console.log(err.message))

        // console.log(this.users);

      // console.log(query);
      // console.log(updatedURL);
      // console.log(this.users.login);

      // this.checkQuery()

      // if(query == this.users.login) {
      //   this.userExists = true
      // } else {
      //   this.userExists = false
      // }
      
      
      // console.log(query);
      // console.log(this.users.login);
      // console.log(this.userExists);
    },

    // checkQuery() {
    //   console.log(this.query);
    // }
  },
}
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&display=swap>');
</style>
