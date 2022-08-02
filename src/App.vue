<template>
  <nav>
    <a>
      <router-link to="/">Home</router-link> |
      <router-link to="/movies">Movies</router-link>
    </a>
  </nav>
  <router-view />
</template>

<style lang="scss">
html {
  background-color: #4c1e10;
}
#app {
  zoom: 80%;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #24e085;
}

nav {
  padding: 30px;
  background-color: 4c1e10;
  position: sticky;
  top: 0;
  z-index: 10000;
  text-align: left;

  a {
    font-weight: bold;
    font-size: 25px;
    color: #cbec14;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
