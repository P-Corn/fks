<template>
  <div class="home">
    <ScoreCard />
  </div>
</template>

<script>
import ScoreCard from '../components/ScoreCard' 

export default {
  name: 'Home',
  components: {
    ScoreCard
  },
  data: function() {
    return {
      
    }
  }
}
</script>

<style lang="scss">
.home {
  height: 100%; //Allows the view to take up the entire screen
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
