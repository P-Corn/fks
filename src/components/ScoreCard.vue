<template>
    <v-sheet
        class="score-card d-flex flex-column"
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

        <v-container class="score-card-chart d-flex flex-column">
            <!-- FKS icons at the top -->
            <v-row 
            class="chart-header pb-3"
            justify-content="space-around"
            no-gutters
            >
                <v-col class="chart-header-icon">
                    <v-icon large>mdi-silverware-fork</v-icon>
                </v-col>
                <v-col class="chart-header-icon">
                    <v-icon large>mdi-knife</v-icon>
                </v-col>
                <v-col class="chart-header-icon">
                    <v-icon large>mdi-silverware-spoon</v-icon>
                </v-col>
            </v-row>
            <!-- Score results -->
            <div class="chart-score d-flex flex-column">
                <v-row 
                v-for="(row,index) in scoreLog"
                :key="index"
                class="score-row"
                justify-content="space-around"
                no-gutters
                >
                    <v-col 
                    class="score-col d-flex justify-center align-center"
                    >
                        <div class="score-amount">
                            {{row.forks}}
                            {{row.winner}}
                        </div>
                    </v-col>
                    <!-- POTENTIAL DIVIDER TO ADD SEPARATION -->
                    <!-- <v-divider vertical></v-divider> -->
                    <v-col 
                    class="score-col d-flex justify-center align-center"
                    >
                        <div class="score-amount">
                            {{row.knives}}
                        </div>
                    </v-col>
                    <!-- <v-divider vertical></v-divider> -->
                    <v-col 
                    class="score-col d-flex justify-center align-center"
                    >
                        <div class="score-amount">
                            {{row.spoons}}
                        </div>
                    </v-col>                  
                </v-row>
            </div>
        </v-container>
    </v-sheet>
</template>

<script>
// @ is an alias to /src


export default {
  name: 'ScoreCard',
  components: {

  },
  methods: {
    winner: function() {
        // this.scoreLog.winner = 9
        
        }
    },
    mounted() {
         this.winner()       
    },
    data: function() {
      return {
          title: "6",

          scoreLog: [
            {
            winner: null,
            forks: "9",
            knives: "3",
            spoons: "8"
            },
            {
            winner: null,
            forks: "3",
            knives: "7",
            spoons: "5"
            },
            {
            winner: null,
            forks: "10",
            knives: "0",
            spoons: "1"
            },
            {
            winner: null,
            forks: "10",
            knives: "0",
            spoons: "1"
            },
            {
            winner: null,
            forks: "0",
            knives: "0",
            spoons: "1"
            },
            {
            winner: null,
            forks: "7",
            knives: "8",
            spoons: "9"
            },
            {
            winner: null,
            forks: "15",
            knives: "2",
            spoons: "8"
            },
          ],
    }
  }
}
</script>

<style lang="scss">
.score-card-header {
    display: flex;
    justify-content: space-between;
}

.score-card-chart {
    height: 100%;
}

.chart-score {
    height: 100%;
    .score-col {

    }
}


</style>