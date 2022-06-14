<template>
  <div id="app">
    <div class="container">
      <header>
        <HeaderSection :darkMode="darkMode" />
      </header>
      <main>
        <SearchBar @update-query="updateQuery($event)" :darkMode="darkMode" :userExists="userExists" :users="users"/>
        <ProfileSection v-if="users.login" :darkMode="darkMode" :users="users" />
        <EmptySearch v-if="!users.login"/>
      </main>
    </div>
  </div>
</template>

<script>
import HeaderSection from './components/HeaderSection.vue'
import SearchBar from './components/SearchBar.vue'
import ProfileSection from './components/ProfileSection.vue'
import EmptySearch from './components/EmptySearch.vue'

export default {
  name: 'App',
  components: {
    HeaderSection,
    SearchBar,
    ProfileSection,
    EmptySearch,
  },

  data() {
    return {
      darkMode: false,
      users: {},
      query: '',
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
      this.userExists = this.users.login == query
      console.log(this.userExists);
      console.log(this.users.login);
      // console.log(this.users.login || query);

      // this.checkQuery()

      // if(this.userExists == this.users.login) {
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
