<template>
    <v-sheet
        class="score-card"
        rounded
        color="white"
        height="300"
        width="200"
    >
    </v-sheet>
</template>

<script>
// @ is an alias to /src


export default {
  name: 'ScoreCard',
  components: {

  }
}
</script>

<style lang="scss">
.score-card {
    //ISSUE: Unable to use "elevation" attribute on v-sheet component. Can't override box-shadow without this style.
    box-shadow: 0 2px 4px -1px rgba(0,0,0,.2),0 4px 5px 0 rgba(0,0,0,.14),0 1px 10px 0 rgba(0,0,0,.12) !important;
}
</style>