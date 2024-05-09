<template>
  <div class="frame">
    <div class="center">
      <div class="circle">
        <div class="sky"></div>
        <div class="sun"></div>
        <div class="side-left"></div>
        <div class="side-right"></div>
        <div class="shadow"></div>
        <div class="ground"></div>
      </div>
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
  border-radius: 2px;
  box-shadow: 1px 2px 10px 0 rgba(0, 0, 0, 0.3);
  background: #272c34;
  color: #fff;
}
.center {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
.circle {
  position: relative;
  width: 180px;
  height: 180px;
  border-radius: 50%;
  clip-path: circle(90px at 90px 90px);
  overflow: hidden;
  .sky {
    position: absolute;
    background-color: #7ddffc;
    height: 124px;
    z-index: 0;
    top: 0;
    left: 0;
    right: 0;
    animation: sky-turn-black 4s cubic-bezier(0.4, 0, 0.49, 1) infinite;
  }
  .sun {
    position: absolute;
    background: #ffef00;
    height: 34px;
    width: 34px;
    z-index: 2;
    top: 7px;
    left: 73px;
    border-radius: 50%;
    transform-origin: 50% 400%;
    animation: sun-goes-down 4s cubic-bezier(0.4, 0, 0.49, 1) infinite;
  }
  .side-left {
    position: absolute;
    top: 67px;
    left: 35px;
    height: 57px;
    width: 116px;
    background: #f4f4f4;
    clip-path: polygon(0% 100%, 50% 0%, 100% 100%);
    animation: pyramid-shading 4s cubic-bezier(0.4, 0, 0.49, 1) infinite;
  }
  .side-right {
    position: absolute;
    top: 67px;
    left: 93px;
    height: 57px;
    width: 58px;
    background: #dddada;
    clip-path: polygon(30% 100%, 0% 0%, 100% 100%);
    animation: pyramid-shading 4s cubic-bezier(0.4, 0, 0.49, 1) infinite reverse;
  }
  .shadow {
    position: absolute;
    z-index: 2;
    top: 124px;
    left: -80px;
    height: 30px;
    width: 360px;
    transform-origin: 50% 0%;
    background: rgba(0, 0, 0, 0.2);
    clip-path: polygon(115px 0%, 231px 0%, 80% 100%);
    animation: shadow-on-the-floor 4s cubic-bezier(0.4, 0, 0.49, 1) infinite;
  }
  .ground {
    position: absolute;
    z-index: 1;
    top: 124px;
    left: 0;
    right: 0;
    height: 56px;
    background: #f0de75;
    animation: fading-ground 4s cubic-bezier(0.4, 0, 0.49, 1) infinite;
  }
}
@keyframes sky-turn-black {
  0% {
    background-color: #272c34;
  }
  30% {
    background-color: #7ddffc;
  }
  70% {
    background-color: #7ddffc;
  }
  100% {
    background-color: #272c34;
  }
}
@keyframes sun-goes-down {
  0% {
    background-color: #f57209;
    transform: rotate(-70deg);
  }
  30% {
    background-color: #ffef00;
    transform: rotate(-28deg);
  }
  70% {
    background-color: #ffef00;
  }
  100% {
    background-color: #f57209;
    transform: rotate(70deg);
  }
}
@keyframes pyramid-shading {
  0% {
    background: #272c34;
  }
  30% {
    background: #f4f4f4;
  }
  70% {
    background: #dddada;
  }
  100% {
    background: #272c34;
  }
}
@keyframes shadow-on-the-floor {
  0% {
    transform: scale(1, 0);
    clip-path: polygon(115px 0%, 231px 0%, 100% 100%);
  }
  30% {
    transform: scale(1, 1);
    clip-path: polygon(115px 0%, 231px 0%, 80% 100%);
  }
  55% {
    transform: scale(1, 0.4);
  }
  75% {
    transform: scale(1, 1);
  }
  100% {
    transform: scale(1, 0);
    clip-path: polygon(115px 0%, 231px 0%, 0% 100%);
  }
}
@keyframes fading-ground {
  0% {
    background: #272c34;
  }
  30% {
    background: #f0de75;
  }
  70% {
    background: #f0de75;
  }
  100% {
    background: #272c34;
  }
}
</style>