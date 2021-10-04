<template>
  <div id="app">
    <Header @selectGenres="selectGenres"/>
    <Albums/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Albums from './components/Albums.vue'


export default {
  name: 'App',
  components: {
    Header,
    Albums
  },
  methods: {
    selectGenres(selectedGenre) {
      console.log(selectedGenre)
    }
  }
}
</script>

<style lang="scss">
@import './assets/style/common.scss';
</style>
