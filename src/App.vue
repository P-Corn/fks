<template>
  <div id="app">
    <v-app>
      <v-main>
        <router-view/>
        <v-bottom-navigation
        color="teal"
        grow
        app
        >

        <v-btn 
        height="auto"
        >
          <span>Submit Score</span>
          <v-icon>mdi-text-box-plus</v-icon>
        </v-btn>

        <v-btn 
        to="/" 
        height="auto"
        >
          <span>Current Game</span>
          <v-icon>mdi-home</v-icon>
        </v-btn>

        <v-btn 
        to="/about"
        height="auto"
        >
          <span>Previous Games</span>
          <v-icon>mdi-history</v-icon>
        </v-btn>
        
      </v-bottom-navigation>
      </v-main>
    </v-app>
    
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
