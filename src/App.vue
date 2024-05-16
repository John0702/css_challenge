<template>
  <div id="app">
    <div class="item">
      <day-one />
    </div>
    <div class="item">
      <day-two />
    </div>
    <div class="item">
      <day-three />
    </div>
    <div class="item">
      <day-four />
    </div>
    <div class="item">
      <day-five />
    </div>
    <div class="item">
      <day-six />
    </div>
    <div class="item">
      <day-seven />
    </div>
  </div>
</template>

<script>
import DayOne from "./components/DayOne.vue";
import DayTwo from "./components/DayTwo.vue";
import DayThree from "./components/DayThree.vue";
import DayFour from "./components/DayFour.vue";
import DayFive from "./components/DayFive.vue";
import DaySix from "./components/DaySix.vue";
import DaySeven from "./components/DaySeven.vue";

export default {
  name: "App",
  components: {
    DayOne,
    DayTwo,
    DayThree,
    DayFour,
    DayFive,
    DaySix,
    DaySeven,
  },
};
</script>

<style lang="scss" scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  overflow: auto;
  display: flex;
  flex-wrap: wrap;
  height: 100em;
}
.item {
  width: 30%;
  display: inline-block;
  margin: 20px;
  margin-bottom: 20px;
  overflow: auto;
  position: relative;
  z-index: 1;
  transition: 0.3s;
}
</style>
