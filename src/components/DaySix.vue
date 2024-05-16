<template>
  <div class="frame">
    <div class="center">
      <div class="profile">
        <div class="image">
          <div class="circle-1"></div>
          <div class="circle-2"></div>
          <img
            src="https://100dayscss.com/codepen/jessica-potter.jpg"
            width="70"
            height="70"
            alt="Jessica Potter"
          />
        </div>
        <div class="name">Jessica Potter</div>
        <div class="job">Visual Artist</div>
        <div class="actions">
          <button class="btn">Follow</button>
          <button class="btn">Message</button>
        </div>
      </div>
      <div class="stats">
        <div class="box">
          <span class="value">523</span>
          <span class="parameter">Posts</span>
        </div>
        <div class="box">
          <span class="value">1387</span>
          <span class="parameter">Likes</span>
        </div>
        <div class="box">
          <span class="value">146</span>
          <span class="parameter">Follower</span>
        </div>
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
  box-shadow: 1px 2px 10px 0px rgba(0, 0, 0, 0.3);
  background: #ca7c4e;
  background: linear-gradient(to top right, #eebe6c 0%, #ca7c4e 100%);
  color: #786450;
  font-family: "Open Sans", Helvetica, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.center {
  position: absolute;
  top: 50px;
  left: 40px;
  height: 299px;
  width: 320px;
  background: #fff;
  border-radius: 3px;
  overflow: hidden;
  box-shadow: 10px 10px 15px 0 rgba(0, 0, 0, 0.3);
}
.profile {
  float: left;
  width: 200px;
  height: 320px;
  text-align: center;
  .image {
    position: relative;
    width: 70px;
    height: 70px;
    margin: 38px auto 0 auto;
    .circle-1,
    .circle-2 {
      position: absolute;
      box-sizing: border-box;
      width: 76px;
      height: 76px;
      top: -3px;
      left: -3px;
      border-width: 1px;
      border-style: solid;
      border-color: #786450 #786450 #786450 transparent;
      border-radius: 50%;
      transition: all 1.5s ease-in-out;
    }
    .circle-2 {
      width: 82px;
      height: 82px;
      top: -6px;
      left: -6px;
      border-color: #786450 transparent #786450 #786450;
    }
    img {
      display: block;
      border-radius: 50%;
      background: #f5e8df;
    }
    &:hover {
      cursor: pointer;
      .circle-1 {
        transform: rotate(360deg);
      }
      .circle-2 {
        transform: rotate(-360deg);
      }
    }
  }
  .name {
    font-size: 15px;
    font-weight: 600;
    margin-top: 20px;
  }
  .job {
    font-size: 11px;
    line-height: 15px;
  }
  .actions {
    margin-top: 33px;
    .btn {
      display: block;
      width: 120px;
      height: 30px;
      margin: 0 auto 10px auto;
      background: none;
      border: 1px solid #786450;
      border-radius: 15px;
      font-size: 12px;
      font-weight: 600;
      box-sizing: border-box;
      transition: all 0.3s ease-in-out;
      color: #786450;
      &:hover {
        background: #786450;
        color: #fff;
      }
    }
  }
}
.stats {
  float: left;
  .box {
    box-sizing: border-box;
    width: 120px;
    height: 99px;
    background: #f5e8df;
    text-align: center;
    padding-top: 28px;
    transition: all 0.4s ease-in-out;
    &:hover {
      background: #e1cfc2;
      cursor: pointer;
    }
    &:nth-child(2) {
      margin: 1px 0;
    }
  }
  span {
    display: block;
  }
  .value {
    font-size: 18px;
    font-weight: 600;
  }
  .parameter {
    font-size: 11px;
  }
}
</style>