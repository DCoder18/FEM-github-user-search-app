<template>
  <div id="app">
    <div class="container">
      <header>
        <HeaderSection></HeaderSection>
      </header>
      <main>
        <SearchBar></SearchBar>
        <ProfileSection></ProfileSection>
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
  }
}
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&display=swap>');
</style>
