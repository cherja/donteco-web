<template>
  <div>
    <div class="header-block">
      <div class="header-logo-contacts">
        <div class="header-block__logo">
          <img src="../assets/images/header__logo_text.jpg" alt="">
        </div>
        <div class="header__front__contacts">
          <p>Москва <a href="tel: +74953746795">8(495)374-67-95</a></p>
          <p>Ростов-на-Дону <a href="tel: +78633200167">8(863)320-01-67</a></p>
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
    </div>
  </div>
</template>

<style lang="scss">
@import "../helpers";
.header-block {
  height: 100vh;
  width: 80vw;
  margin: auto;
    @include screen-max(350px){
    display: none;
  }
}
.header-logo-contacts {
 display: flex;
 align-items: center;
 justify-content: space-between;
 padding: 2vw 0 5vw 0;
 @include screen-max(1650px) {
    padding: 1vw 0 1.5vw 0;
  }
}
.header-block__logo {
  width: 10vw;
  img {
    width: 100%;
  }
}

.header__front__contacts {
  font-family: "SSP";
  p, a {
    font-size: 1.3vw;
    color: #2e00a7;
  }
  a {
    font-weight: 900;
    text-decoration: none;
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
}
.kvadro {
  animation: kvatro 20s infinite;;
  display: flex;
  position: absolute;
  width: 160vw;
  height:140vh;
  z-index: -1;
}

.a {
  background-image: url(../assets/images/1.jpg);
  background-position: center center;
  background-size: cover;
  background-repeat: no-repeat;
  width: 80vw;
  height:70vh;

}
.b {
  background-image: url(../assets/images/2.jpg);
  background-position: center center;
  background-size: cover;
  background-repeat: no-repeat;
  width: 80vw;
  height:70vh;

}
.c {
  background-image: url(../assets/images/2.jpg);
  background-position: center center;
  background-size: cover;
  background-repeat: no-repeat;
  width: 80vw;
  height:70vh;
}
.d {
  background-image: url(../assets/images/1.jpg);
  background-position: center center;
  background-size: cover;
  background-repeat: no-repeat;
  width: 80vw;
  height:70vh;

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
height:20vw;
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

</style>
