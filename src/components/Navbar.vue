<template>
    <div id="nav">
      <!-- <router-link to="/contact">Contact</router-link> | -->
      <a href="#projects">Projects</a> |
      <a href="#contact">Contact</a>
    </div>
</template>

<style lang="scss">
#nav {
  padding: 30px;
  display: flex;
  justify-content: flex-end;
  a {
    font-weight: bold;
    font-size: 1.4em;
    color: #525f7f;
    margin: 0 0.5em;

    &.router-link-exact-active {
      color: #6292d0;
    }
  }
}
</style>
