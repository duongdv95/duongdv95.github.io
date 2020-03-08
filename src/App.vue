<template>
  <div id="app">
    <Navbar/>
    <router-view/>
  </div>
</template>

<script>
import Navbar from '@/components/Navbar.vue'

export default {
  name: 'home',
  components: {
    Navbar
  }
}
</script>

<style lang="scss">
@import '@/styles/_websiteStyle';

body {
  background-color: $websitecolor;
}

#app {
  font-family: $fontfamily;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: $fontcolor;
  padding: 0 1em;
}

@media (min-width: 600px) {
  #app {
    display: grid;
    grid-template-columns: 1fr minmax(auto, 60em) 1fr;
  }

  #nav, .home, #todos {
    grid-column: 2/3;
  }
  }
</style>
