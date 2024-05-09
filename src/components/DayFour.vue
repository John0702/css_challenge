<template>
  <div class="frame">
    <div class="center">
      <div class="circle-1"></div>
      <div class="circle-2"></div>
      <div class="circle-3"></div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.frame {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 400px;
  height: 400px;
  margin-top: -200px;
  margin-left: -200px;
  border-radius: 5px;
  box-shadow: 1px 2px 10px 0 rgba(0, 0, 0, 0.3);
  overflow: hidden;
  background: #e56262;
  color: #fff;
}
.center {
  position: absolute;
  width: 220px;
  height: 220px;
  top: 90px;
  left: 90px;
}
.circle-1 {
  position: absolute;
  z-index: 1;
  width: 90px;
  height: 90px;
  border-radius: 50%;
  background: #fff;
  top: 65px;
  left: 65px;
  animation: circle-1 2s cubic-bezier(0.21, 0.98, 0.6, 0.99) infinite alternate;
}
.circle-2 {
  position: absolute;
  z-index: 2;
  width: 60px;
  height: 60px;
  border-radius: 50%;
  background: #fff;
  top: 80px;
  left: 80px;
  animation: circle-2 2s cubic-bezier(0.21, 0.98, 0.6, 0.99) infinite alternate;
}
.circle-3 {
  position: absolute;
  z-index: 3;
  width: 30px;
  height: 30px;
  border-radius: 50%;
  background: #fff;
  top: 95px;
  left: 95px;
  animation: circle-3 2s cubic-bezier(0.21, 0.98, 0.6, 0.99) infinite alternate;
}
@keyframes circle-1 {
  0%,
  10% {
    box-shadow: 2px 2px 3px 2px rgba(0, 0, 0, 0.2);
    transform: scale(0);
  }
  100% {
    box-shadow: 10px 10px 15px 0px rgba(0, 0, 0, 0.3);
    transform: scale(1);
  }
}
@keyframes circle-2 {
  0%,
  40% {
    box-shadow: 2px 2px 3px 2px rgba(0, 0, 0, 0.2);
    transform: scale(0);
  }
  100% {
    box-shadow: 10px 10px 15px 0px rgba(0, 0, 0, 0.3);
    transform: scale(1);
  }
}
@keyframes circle-3 {
  0%,
  70% {
    box-shadow: 2px 2px 3px 2px rgba(0, 0, 0, 0.2);
    transform: scale(0);
  }
  100% {
    box-shadow: 10px 10px 15px 0px rgba(0, 0, 0, 0.3);
    transform: scale(1);
  }
}

</style>