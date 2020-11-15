<template>
    <div>
        <v-row 
        class="score-row"
        justify-content="space-around"
        no-gutters
        >
            <v-col 
            class="score-col d-flex justify-center align-center"
            >
                <div 
                class="score-amount d-flex justify-center align-end" 
                :class="[ forkScore > spoonScore && forkScore > knifeScore ? winnerStyle : loserStyle ]"
                >
                    {{forkScore}}
                </div>
            </v-col>
            <!-- POTENTIAL DIVIDER TO ADD SEPARATION -->
            <!-- <v-divider vertical></v-divider> -->
            <v-col 
            class="score-col d-flex justify-center align-center"
            >
                <div 
                class="score-amount d-flex justify-center align-end"
                :class="[ knifeScore > spoonScore && knifeScore > forkScore ? winnerStyle : loserStyle ]"
                >
                    {{knifeScore}}
                </div>
            </v-col>
            <!-- <v-divider vertical></v-divider> -->
            <v-col 
            class="score-col d-flex justify-center align-center"
            >
                <div 
                class="score-amount d-flex justify-center align-end"
                :class="[ spoonScore > forkScore && spoonScore > knifeScore ? winnerStyle : loserStyle ]"
                >
                    {{spoonScore}}
                </div>
            </v-col>                  
        </v-row>
    </div>
</template>

<script>
// @ is an alias to /src


export default {
  name: 'ScoreRow',
  props: {
      forkScore: String,
      knifeScore: String,
      spoonScore: String
  },
  data: function() {
      return {
          loserStyle: "loserStyle",
          winnerStyle: "winnerStyle"
      }
  },
  methods: {
      winner: function() {

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
        .score-amount {
            border-radius: 100px;
            width: 30px;
            height: 30px;
        }
    }
}

.winnerStyle {
    border: 2px solid rgb(133, 255, 170);
}

.loserStyle {
    border: 2px solid white;
}


</style>