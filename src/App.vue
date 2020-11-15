<template>
  <div id="app">
    <router-view/>
      <v-bottom-navigation
        color="teal"
        grow
        app
      >
        <v-btn 
        to="/about"
        height="auto"
        >
          <span>Recent Games</span>

          <v-icon>mdi-history</v-icon>
        </v-btn>

        <v-btn 
        to="/" 
        height="auto"
        >
          <span>Current</span>

          <v-icon>mdi-heart</v-icon>
        </v-btn>

        <v-btn 
        height="auto"
        >
          <span>Nearby</span>

          <v-icon>mdi-map-marker</v-icon>
        </v-btn>
      </v-bottom-navigation>
  </div>
</template>

<style lang="scss">
#app {
  font-family: Roboto, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100vh;
  background-color: #fafafa;
}
</style>
