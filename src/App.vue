<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <Main />
</template>

<script>
import Main from './components/Main.vue'

export default {
  name: 'App',
  components: {
    Main
  }
}
</script>

<style>
*, body { margin: 0; padding: 0; box-sizing: border-box; }
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 20px;
}
li { list-style: none; }
a { text-decoration: none; }
</style>
