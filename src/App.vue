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
body{
  background-color: #f2f2f2;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #525f7f;
  padding: 0 1em;
}

@media (min-width: 600px) {
  #app {
    display: grid;
    grid-template-columns: 1fr minmax(auto, 60em) 1fr;
  }

  #nav, .home {
    grid-column: 2/3;
  }
  }
</style>
