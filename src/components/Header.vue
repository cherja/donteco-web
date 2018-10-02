<template>
<div class="rel">
  <div @click="$emit('open')" class=header__front__call__hd>
    <p>ЗАКАЗАТЬ ЗВОНОК</p>
    <p class="line"></p>
  </div>
  <div class="header">
    <div class="logo-adress">
      <div class="logo-img">
        <img src="../assets/images/header__logo_text.jpg" alt="">
      </div>
      <div class="header__front__contacts">
        <p>Москва <a href="tel: +74953746795">8(495)374-67-95</a></p>
        <p>Ростов-на-Дону <a href="tel: +78633200167">8(863)320-01-67</a></p>
      </div>
    </div>
    <div class="header-animation">
      <div class="all-item">
      <div class="all-item-front">
        <div>
          <div class="one-static zero"></div>
          <div class="two-static zero"></div>
        </div>
        <div>
          <div class="three-static zero"></div>
          <div class="four-static zero"></div>
        </div>
        <div>
          <div class="five-static zero"></div>
          <div class="six-static zero"></div>
        </div>
        <div>
          <div class="seven-static zero"></div>
          <div class="eight-static zero"></div>
        </div>
      </div>
      <div class="all-item-front-mobile">
        <div class="item-front-mobile">
          <div class="item-front-mobile_one"></div>
          <div class="item-front-mobile_two"></div>
        </div>
          <div class="item-front-mobile">
          <div class="item-front-mobile_two"></div>
          <div class="item-front-mobile_three"></div>
        </div>
        <div class="item-front-mobile"></div>
      </div>
      <div class="left-column">
        <div v-show="a" class="item one"></div>
        <div v-show="aa" class="item onea"></div>
        <div v-show="e" class="item five"></div>
        <div v-show="b" class="item two"></div>
        <div v-show="bb" class="item twoa"></div>
        <div v-show="f" class="item six"></div>
        <div class="mobile-left-bottom"></div>
      </div>
      <div class="right-column">
        <div v-show="c"  class="item three"></div>
        <div v-show="cc"  class="item threea"></div>
        <div v-show="g"  class="item seven"></div>
        <div v-show="d" class="item four"></div>
        <div v-show="dd" class="item foura"></div>
        <div v-show="h"  class="item eight"></div>
        <div class="mobile-right-bottom"></div>
      </div>
    </div>
    </div>
    <div class="mobile-adress-button">
      <p>Москва <a href="tel: +74953746795">8(495)374-67-95</a></p>
      <p>Ростов-на-Дону <a href="tel: +78633200167">8(863)320-01-67</a></p>
      <button @click="$emit('open')">Заказать звонок</button>
    </div>
  </div>
</div>
</template>

<script>
export default {
  mounted () {
    this.addMedia()
  },
  data () {
    return {
      aa: true,
      bb: true,
      cc: true,
      dd: true,
      a: false,
      b: false,
      c: false,
      d: false,
      e: false,
      f: false,
      g: false,
      h: false
    }
  },
  methods: {
    addMedia () {
      let i = -13
      setInterval((
      ) => {
        if (i === -11) {
          this.bb = false
          this.b = true
        }
        if (i === -10) {
          this.aa = false
          this.a = true
        }
        if (i === -9) {
          this.cc = false
          this.c = true
        }
        if (i === -8) {
          this.dd = false
          this.d = true
        }
        if (i === 0) {
          this.b = false
          this.f = true
        }
        if (i === 1) {
          this.a = false
          this.e = true
        }
        if (i === 2) {
          this.c = false
          this.g = true
        }
        if (i === 3) {
          this.d = false
          this.h = true
        }

        if (i === 11) {
          this.f = false
          this.b = true
        }
        if (i === 12) {
          this.e = false
          this.a = true
        }
        if (i === 13) {
          this.g = false
          this.c = true
        }
        if (i === 14) {
          this.h = false
          this.d = true
        }
        i++
        if (i === 22) {
          i = 0
        }
      }, 1200)
    }
  }
}
</script>

<style lang="scss">
@import "../helpers";
.mobile-adress-button {
  display: none;
  font-family: "SSP";
  text-align: left;
  width: 90vw;
  margin:auto;
  p, a {
    color: #2e00a7;
    font-weight: 900;
    text-decoration: none;
    @include screen-sm {
      font-size: 2.3vw;
    }
    @include screen-xs {
      font-size: 3.5vw;
    }
  }
  p {
    font-weight: 400;
  }
  button {
    margin-top: 20px;
    border: none;
    padding: 2px 8px;
    background: #11449d;
    border-radius: 3px;
    color:white;
    @include screen-sm {
      font-size: 2.3vw;
    }
    @include screen-xs {
      font-size: 3.5vw;
    }
  }
  @include screen-sm {
    display: block;
  }
}
.rel {
  position: relative;
  backface-visibility: hidden;
}
.header__front__call__hd {
  font-weight: 900;
  z-index: 9999;
  display: flex;
  align-items: center;
  position: absolute;
  transform-origin: 0px 0px;
  transform: rotate(-90deg);
  bottom: 30vh;
  right: -650px;
  font-size: 27px;
  color: #11449d;
  cursor: pointer;
  @include screen-max(1600px) {
    font-size: 25px;
  }
  @include screen-max(1400px) {
    font-size: 23px;
  }
  @include screen-max(1200px) {
    right: -660px;
  }
  @include screen-max(1100px) {
    right: -670px;
  }
  @include screen-sm {
    display: none;
  }
}
.line {
 width: 500px;
 border: 1px solid #11449d;
 background-color: #11449d;
}
.header__front__contacts {
  font-family: "SSP";
  text-align: right;
  p, a {
    font-size: 1.5vw;
    color: #2e00a7;
    font-weight: 900;
    text-decoration: none;
  }
   @include screen-sm {
    display: none;
  }

}
.logo-img {
   width: 13vw;
   @include screen-lg {
    width: 11vw;
  }
  @include screen-sm{
    width: 22vw;
  }
}
img {
  width: 100%;
}
.logo-adress {
  margin: auto;
  align-items: center;
  width: 80vw;
  height: 20vh;
  display: flex;
  position: relative;
  justify-content: space-between;
  z-index: 9999;
  @include screen-sm {
    width: 90vw;
    height: 10vh;
  }
}
.item-front-mobile {
 display: flex;
}
.item-front-mobile_one {
  width: 45vw;
  height: 23vh;
  background-image: url(../assets/images/1.jpg);
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center center;
}
.item-front-mobile_two {
  width: 45vw;
  height: 23vh;
}
.item-front-mobile_three {
  width: 45vw;
  height: 23vh;
  background-image: url(../assets/images/4.jpg);
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center center;
}
.all-item-front-mobile {
  z-index: 999;
  display: none;
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  @include screen-sm {
    display: block;
  }
}
.mobile-left-bottom{
  display: none;
  width: 45vw;
  height: 23vh;
  background-image: url(../assets/images/5.jpg);
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center center;
  @include screen-sm {
    display: flex;
  }
}
.mobile-right-bottom{
    display: none;
  width: 45vw;
  height: 23vh;
     background-image: url(../assets/images/2.jpg);
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center center;
  @include screen-sm {
    display: flex;
  }
}
.header {
  height: 100vh;
}
.left-column {
  z-index: 90;
}
.right-column {
  z-index: 80;
}
.header-animation {
  margin: auto;
  width: 80vw;
  height: 70vh;
  overflow: hidden;
  @include screen-sm {
  width: 90vw;
  height: 75vh;
  }
}
.all-item {
  margin: auto;
  position: relative;
  display: flex;
  width: 80vw;
  height: 90vh;
  align-items: center;
  justify-content: center;
  background-image: url(../assets/images/3.png);
    background-size: cover;
  background-repeat: no-repeat;
  @include screen-sm {
    width: 90vw;
    height: 69vh;
  }
}
.all-item-front {
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  display: flex;
  z-index: 99;
   @include screen-sm {
    display: none;
  }
}
.item {
  background-size: cover;
  background-repeat: no-repeat;
}
.zero {
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center center;
  width: 20vw;
}
.one-static {
  background-image: url(../assets/images/1.jpg);
  height: 45vh;
}
.two-static {
  background-image: url(../assets/images/2.jpg);
  height: 25vh;
}

.three-static {
  background-image: url(../assets/images/3.png);
  height: 45vh;
}
.four-static {
  height: 25vh;
}
.five-static {
  height: 45vh;
}
.six-static {
  background-image: url(../assets/images/4.jpg);
  height: 25vh;
}
.seven-static {
  background-image: url(../assets/images/5.jpg);
  height: 45vh;
}
.eight-static {
  height: 25vh;
  background-image: url(../assets/images/6.png);
}

.one {
  animation: translate-left .7s;
  width: 40vw;
  height: 45vh;
  background-position: right bottom;
  background-image: url(../assets/images/a.jpg);
  @include screen-sm {
    width: 45vw;
    height: 23vh;
  }
}
.onea {
  width: 40vw;
  height: 45vh;
  background-position: right bottom;
  background-image: url(../assets/images/e.jpg);
    @include screen-sm {
    width: 45vw;
    height: 25vh;
  }
}
.two {
  animation: translate-left .7s;
  width: 40vw;
  height: 45vh;
  background-position: top right;
  background-image: url(../assets/images/b.jpg);
    @include screen-sm {
    width: 45vw;
    height: 23vh;
  }
}
.twoa {
  width: 40vw;
  height: 45vh;
  background-position: top right;
  background-image: url(../assets/images/f.jpg);
    @include screen-sm {
    width: 45vw;
    height: 23vh;
  }
}
.three {
  animation: translate-left .7s;
  width: 40vw;
  height: 45vh;
  background-position: left bottom;
  background-image: url(../assets/images/c.jpg);
    @include screen-sm {
    width: 45vw;
    height: 23vh;
  }
}
.threea {
  width: 40vw;
  height: 45vh;
  background-position: left bottom;
  background-image: url(../assets/images/g.jpg);
    @include screen-sm {
    width: 45vw;
    height: 23vh;
  }
}
.foura {
  width: 40vw;
  height: 45vh;
  background-position: left top;
  background-image: url(../assets/images/h.jpg);
    @include screen-sm {
    width: 45vw;
    height: 23vh;
  }
}
.four {
  animation: translate-left .7s;
  width: 40vw;
  height: 45vh;
  background-position: left top;
  background-image: url(../assets/images/d.jpg);
    @include screen-sm {
    width: 45vw;
    height: 23vh;
  }
}

.five {
  animation: translate-left .7s;
  width: 40vw;
  height: 45vh;
  background-position: right bottom;
  background-image: url(../assets/images/e.jpg);
    @include screen-sm {
    width: 45vw;
    height: 23vh;
  }
}
.six {
  animation: translate-left .7s;
  width: 40vw;
  height: 45vh;
  background-position: top right;
  background-image: url(../assets/images/f.jpg);
    @include screen-sm {
    width: 45vw;
    height: 23vh;
  }
}

.seven{
  animation: translate-left .7s;
  width: 40vw;
  height: 45vh;
  background-position: left bottom;
  background-image: url(../assets/images/g.jpg);
    @include screen-sm {
    width: 45vw;
    height: 23vh;
  }
}

.eight{
  animation: translate-left .7s;
  width: 40vw;
  height: 45vh;
  background-position: left top;
  background-image: url(../assets/images/h.jpg);
    @include screen-sm {
    width: 45vw;
    height: 23vh;
  }
}

@keyframes translate-left {
  0% {
    transform: translateX(-40vw);
  }
  100% {
    transform: translateX(0vw);
  }
}
</style>
