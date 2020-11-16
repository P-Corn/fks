<template>
  <div id="app">
    <v-app>
      <AppBar />
      <v-main>
        <router-view />
      </v-main>
    </v-app>
    
  </div>
</template>

<script>
import AppBar from './components/AppBar'

export default {
  name: 'App',
  components: {
    AppBar
  }
}
</script>

<style lang="scss">
#app {
  font-family: Roboto, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  // height: 100px;
  background-color: #fafafa;
}

body {
  overflow: hidden;
}
</style>
