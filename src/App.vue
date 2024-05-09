<template>
  <div id="app">
    <!-- <day-one/> -->
    <!-- <day-two/> -->
    <!-- <day-three/> -->
    <!-- <day-four/> -->
    <day-five/>
  </div>
</template>

<script>
// import DayOne from './components/DayOne.vue'
// import DayTwo from './components/DayTwo.vue'
// import DayThree from './components/DayThree.vue'
// import DayFour from './components/DayFour.vue'
import DayFive from './components/DayFive.vue'

export default {
  name: 'App',
  components: {
    // DayOne,
    // DayTwo
    // DayThree
    // DayFour
    DayFive
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
  display: flex;
}
</style>
