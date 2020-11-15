<template>
    <v-sheet
        class="score-card"
        rounded
        elevation="3"
        color="white"
        height="400"
        width="300"
    >
        <v-subheader class="score-card-header">
            <div class="score-card-id">1</div>
            <div class="score-card-date">12/14 - 12/20</div>
        </v-subheader>

        <v-divider></v-divider>

        <v-container class="score-card-chart">
            <v-row class="chart-header"
            justify-content="space-around"
            no-gutters
            >
                <v-col class="chart-header-icon">
                    <v-icon>mdi-silverware-fork</v-icon>
                </v-col>
                <v-col class="chart-header-icon">
                    <v-icon>mdi-knife</v-icon>
                </v-col>
                <v-col class="chart-header-icon">
                    <v-icon>mdi-silverware-spoon</v-icon>
                </v-col>
            </v-row>

            <v-container class="chart-score">
                <div class="chart-score-row">
                    <v-row

                    >
                    <v-cols>
                        <div>hi</div>
                    </v-cols>
                    </v-row>
                </div>
            </v-container>
        </v-container>
    </v-sheet>
</template>

<script>
// @ is an alias to /src


export default {
  name: 'ScoreCard',
  components: {

  },
  data () {
      return {
          title: 'string',

          scoreLog: [
            {
            forks: "8",
            knives: "4",
            spoons: "5"
            },
            {
            forks: "8",
            knives: "4",
            spoons: "5"
            },
          ]
  }
}
</script>

<style lang="scss">
.score-card-header {
    display: flex;
    justify-content: space-between;
}

.score-card-chart {
    .chart-header {
        // padding-top: 10px;
    }
}
</style>