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
            <div 
            class="chart-score d-flex flex-column"
            v-for="(row,index) in scoreLog"
            :key="index"
            >
                <ScoreRow 
                :forkScore="row.forks"
                :knifeScore="row.knives"
                :spoonScore="row.spoons"
                />
            </div>
        </v-container>
    </v-sheet>
</template>

<script>
import ScoreRow from './ScoreRow.vue'

export default {
  name: 'ScoreCard',
  components: {
      ScoreRow
  },
  methods: {
    
    },
    data: function() {
      return {

          scoreLog: [
            {
            forks: 9,
            knives: 3,
            spoons: 8
            },
            {
            forks: 3,
            knives: 9,
            spoons: 5
            },
            {
            forks: 10,
            knives: 0,
            spoons: 1
            },
            {
            forks: 10,
            knives: 0,
            spoons: 1
            },
            {
            forks: 0,
            knives: 0,
            spoons: 1
            },
            {
            forks: 7,
            knives: 8,
            spoons: 9
            },
            {
            forks: 15,
            knives: 5,
            spoons: 2
            },
          ],
    mounted() {
        this.winner()       
    },
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