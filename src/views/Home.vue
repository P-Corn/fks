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
  }
}
</script>

<style lang="scss">
.home {
  height: 100%; //Allows the view to take up the entire screen
  padding-bottom: 56px;  //Height of bottom nav
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
