<template>
  <div>
    <div class="header-block">
      <div @click="$emit('open')" class=header__front__call__hd>
        <p>ЗАКАЗАТЬ ЗВОНОК</p>
        <p class="line"></p>
      </div>
      <div class="header-logo-contacts">
        <div class="header-block__logo">
          <img src="../assets/images/header__logo_text.jpg" alt="">
        </div>
        <div class="header__front__contacts">
          <p>Москва <a href="tel: +74953746795">8(495)374-67-95</a></p>
          <p>Ростов-на-Дону <a href="tel: +78633200167">8(863)320-01-67</a></p>
        </div>
      </div>
      <div class="item-mobile">
        <div class="kvadro-mobile">
              <div>
            <div class="a" ></div>
            <div class="b" ></div>
          </div>
          <div>
            <div class="c"></div>
            <div class="d"></div>
          </div>
        </div>
        <div>
          <div class="one-mobile zero"></div>
          <div class="two-mobile"></div>
          <div class="three-mobile zero"></div>
        </div>
        <div>
          <div class="two-mobile"></div>
          <div class="five-mobile zero"></div>
          <div class="two-mobile"></div>
        </div>
        <div class="two-column-mobile">

        </div>
      </div>
      <div class="item">
        <div class="kvadro">
          <div>
            <div class="a" ></div>
            <div class="b" ></div>
          </div>
          <div>
            <div class="c"></div>
            <div class="d"></div>
          </div>
        </div>
        <div>
          <div class="one zero"></div>
          <div class="two zero"></div>
        </div>
        <div>
          <div class="five zero"></div>
          <div class="six zero"></div>
        </div>
        <div>
          <div class="seven zero"></div>
          <div class="eight zero"></div>
        </div>
        <div>
          <div class="three zero"></div>
          <div class="four zero"></div>
        </div>
      </div>
      <div class="header__front__contacts mobile-text">
        <p>Москва <a href="tel: +74953746795">8(495)374-67-95</a></p>
        <p>Ростов-на-Дону <a href="tel: +78633200167">8(863)320-01-67</a></p>
      </div>
      <button @click="$emit('open')">ЗАКАЗАТЬ ЗВОНОК</button>
    </div>
  </div>
</template>

<style lang="scss">
@import "../helpers";
.item-mobile {
  position: relative;
  display: none;
  width: 90vw;
  height:72vh;
  overflow: hidden;
   @include screen-sm {
    display: flex;
  }
}
.one-mobile {
  background-image: url(../assets/images/4.jpg);
  width: 45vw;
  height: 24vh;
}
.two-mobile {
  width: 45vw;
  height: 24vh;
}
.three-mobile {
  background-image: url(../assets/images/6.jpg);
  width: 45vw;
  height: 24vh;
}

.five-mobile {
  background-image: url(../assets/images/road.jpg);
  width: 45vw;
  height: 24vh;
}
button {
  display: none;
  @include screen-sm {
  display: block;
  letter-spacing: 2px;
  font-family: Geneva;
  font-size: 3vw;
  background-color: #2e00a7;
  color: #ffffff;
  border: none;
  border-radius: 3px;
  padding: 2px 10px;
  margin: 10px 0;
  }
}
.header-block {
  height: 100vh;
  width: 80vw;
  margin: auto;
  position: relative;
   @include screen-sm {
    // height: auto;
  }
}
.header-logo-contacts {
 display: flex;
 align-items: center;
 justify-content: space-between;
 padding: 2vw 0 5vw 0;
 @include screen-max(1650px) {
    padding: 2vw 0 1.5vw 0;
  }
}
.header-block__logo {
  width: 10vw;
  img {
    width: 100%;
  }
  @include screen-sm {
    width: 20vw;
  }
}

.header__front__contacts {
  font-family: "SSP";
  p, a {
    font-size: 1.3vw;
    color: #2e00a7;
    @include screen-sm {
      font-size: 3vw;
    }
  }
  a {
    font-weight: 900;
    text-decoration: none;
  }
  @include screen-sm {
    display: none;
    margin: 40px 0;
  }
}

.mobile-text {
  display: none;
  @include screen-sm {
    display: block;
  }
}

.item {
  display: flex;
  justify-content: space-between;
  width: 80vw;
  height:70vh;
  position: relative;
  overflow: hidden;
  @include screen-max(1750px) {
    margin: 3vw 0;
  }
  @include screen-sm {
    display: none;
  }
}

.header__front__call__hd {
  font-weight: 900;
  z-index: 2;
  display: flex;
  align-items: center;
  position: absolute;
  transform-origin: 0px 0px;
  transform: rotate(-90deg);
  bottom: 35vh;
  right:-800px;
  font-size: 27px;
  color: #11449d;
  cursor: pointer;
  @include screen-max(1400px) {
    // display: none;
    font-size: 20px;
    right:-730px;
  }
  @include screen-max(1200px) {
    // display: none;
    font-size: 16px;
    right:-680px;
  }
  @include screen-sm {
    display: none;
  }
}

.line {
 width: 500px;
 border: 1px solid #11449d;
}
.kvadro {
  animation: kvatro 20s infinite;;
  display: flex;
  position: absolute;
  width: 160vw;
  height:140vh;
  z-index: -1;
}
.kvadro-mobile {
  animation: kvadro-mobile 20s infinite;;
  display: flex;
  position: absolute;
  width: 180vw;
  height:144vh;
  z-index: -1;
}

.a {
  background-image: url(../assets/images/1.jpg);
  background-position: center center;
  background-size: cover;
  background-repeat: no-repeat;
  width: 80vw;
  height:70vh;
  @include screen-sm {
    width: 90vw;
    height:72vh;
  }

}
.b {
  background-image: url(../assets/images/2.jpg);
  background-position: center center;
  background-size: cover;
  background-repeat: no-repeat;
  width: 80vw;
  height:70vh;
   @include screen-sm {
    width: 90vw;
    height:72vh;
  }

}
.c {
  background-image: url(../assets/images/2.jpg);
  background-position: center center;
  background-size: cover;
  background-repeat: no-repeat;
  width: 80vw;
  height:70vh;
   @include screen-sm {
    width: 90vw;
    height:72vh;
  }
}
.d {
  background-image: url(../assets/images/1.jpg);
  background-position: center center;
  background-size: cover;
  background-repeat: no-repeat;
  width: 80vw;
  height:70vh;
   @include screen-sm {
    width: 90vw;
    height:72vh;
  }
}
.zero {
  background-position: center center;
  background-size: cover;
  background-repeat: no-repeat;
}

.one {
background-image: url(../assets/images/4.jpg);
width: 20vw;
height:50vh;
}
.two {
width: 20vw;
height:20vh;
background-image: url(../assets/images/5.jpg);
}
.three {
width: 20vw;
height:20vh;
background-image: url(../assets/images/6.jpg);
}
.four {
width: 20vw;
height:50vh;
background-image: url(../assets/images/7.png);
}
.five {
width: 20vw;
height:50vh;
background-image: url(../assets/images/8.png);
}
.six {
width: 20vw;
height:20vh;
}
.seven {
width: 20vw;
height:50vh;
}
.eight {
width: 20vw;
height:20vh;
background-image: url(../assets/images/road.jpg);
}

@keyframes kvatro {
  20% {
    transform: translateX(0vw);
  }
  25% {
    transform: translateX(-80vw);
  }
  45% {
    transform: translateX(-80vw);
  }
  50% {
    transform: translate(-80vw, -70vh);
  }
  70% {
    transform: translate(-80vw, -70vh);
  }
  75% {
    transform: translate(0vw, -70vh);
  }
  95% {
    transform: translate(0vw, -70vh);
  }
}
@keyframes kvadro-mobile {
  20% {
    transform: translateX(0vw);
  }
  25% {
    transform: translateX(-90vw);
  }
  45% {
    transform: translateX(-90vw);
  }
  50% {
    transform: translate(-90vw, -72vh);
  }
  70% {
    transform: translate(-90vw, -72vh);
  }
  75% {
    transform: translate(0vw, -72vh);
  }
  95% {
    transform: translate(0vw, -72vh);
  }
}
</style>
