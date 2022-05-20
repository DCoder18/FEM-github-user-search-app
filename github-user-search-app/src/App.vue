<template>
  <div id="app">
    <div class="container">
      <header>
        <HeaderSection></HeaderSection>
      </header>
      <main>
        <SearchBar></SearchBar>
      </main>
    </div>
  </div>
</template>

<script>
import HeaderSection from './components/HeaderSection.vue'
import SearchBar from './components/SearchBar.vue'

export default {
  name: 'App',
  components: {
    HeaderSection,
    SearchBar,
  }
}
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&display=swap>');
</style>
