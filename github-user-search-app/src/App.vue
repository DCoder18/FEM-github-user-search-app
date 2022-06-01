<template>
  <div id="app">
    <div class="container">
      <header>
        <HeaderSection :darkMode="darkMode" />
      </header>
      <main>
        <SearchBar :darkMode="darkMode" />
        <ProfileSection :darkMode="darkMode" />
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
    }
  },

  methods: {
    dark() {
      document.querySelector('body').classList.add('dark-mode')
      this.darkMode = true
      this.$emit('dark')
    },

    light() {
      document.querySelector('body').classList.remove('dark-mode')
      this.darkMode = false
      this.$emit('light')
    },

    modeToggle() {
      if(this.darkMode || document.querySelector('body').classList.contains('dark-mode')) {
          this.light()
      } else {
          this.dark()
      }
    },
  },
}
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&display=swap>');
</style>
