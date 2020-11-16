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
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
}
</style>
