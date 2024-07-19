<template>
  <div class="app">
    <div class="main-container">
      <Header />
      <NavBar />
      <component :is="showActiveComponent()" />
    </div>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import NavBar from './components/NavBar.vue'
import Home from './components/Home.vue'

export default {
  data() {
    return {
      activatePage: 'home'
    }
  },
  components: {
    Header,
    NavBar,
    Home
  },
  methods: {
    showActiveComponent() {
      const components = {
        'home': Home
      }
      return components[self.activatePage] || Home
    }
  }
}
</script>

<style>
  .main-container {
    width: 100%;
    height: 3160px;
    margin: 0 auto;
    max-width: 1200px;
    border: 2px solid black;
  }
</style>