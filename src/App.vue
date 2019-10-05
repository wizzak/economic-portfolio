<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
      <router-link to="/projects">Projects</router-link>
      <router-link to="/contact">Contact</router-link>
    </div>
    <router-view />
    <footer>
      <div class="footer-menu">
        <router-link to="/">Impressum</router-link>
        <router-link to="/">Datenschutz</router-link>
      </div>
    </footer>
  </div>
</template>

<style lang="scss">
body {
  background-color: #101010;
  font-size: 20px;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Ubuntu,
    "Helvetica Neue", Arial, sans-serif;
}
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #fff;
  position: relative;
  min-height: 95vh;
  margin: 0 15px;
}
#nav {
  padding: 30px;
  display: flex;
  justify-content: end;
  a {
    margin-left: 112px;
    text-decoration: none;
    font-size: 24px;
    font-weight: 400;
    letter-spacing: 5px;
    color: #fff;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
footer {
  color: #fff;
  position: absolute;
  bottom: 10px;
  right: 30px;
  .footer-menu {
    display: flex;
    justify-content: end;
    a {
      color: #4e4e4e;
      text-decoration: none;
      margin-left: 20px;
      font-size: 0.8em;
    }
  }
}
</style>
