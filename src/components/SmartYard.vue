<template>
  <div class="smart-yard-block container">
    <div class="smart-yard-block__text">
      <h2>SMART YARD</h2>
      <h3>Удаленное управления СКУД системой</h3>
      <p>Мобильные приложения для iOS и Android, позволяющие удаленно управлять СКУД-системой от компании ООО Бастион. Никогда еще комплексная защита частного домовладения не была такой удобной и информативной</p>
    </div>
    <div class="smart-yard-block__img">
      <div class="smart-yard-block__img-mobile smart-yard-block__img-yard-one"></div>
      <div class="smart-yard-block__img-mobile smart-yard-block__img-yard-two"></div>
    </div>
  </div>
</template>

<style lang="scss">
@import "../helpers";

.smart-yard-block {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 100px 0;
   @include screen-md {
    justify-content: flex-start;
   }
   @include screen-xs {
    display: block;
    margin: 50px 0;
  }
}

.smart-yard-block__text{
  @include screen-xs {
     margin: auto;
    width: 310px;
  }
  h2 {
    font-family: "BBB";
    font-weight: 900;
    font-size: 78px;
    color: #0039b4;
    @include screen-max(1850px) {
      font-size: 62px;
    }

    @include screen-max(1400px) {
      font-size: 50px;
    }

    @include screen-lg {
      font-size: 48px;
    }
  }

  h3 {
    font-family: "SSP";
    font-size: 43px;
    font-weight: 100;
    line-height:1.1;
     @include screen-max(1850px) {
      font-size: 35px;
    }

    @include screen-max(1400px) {
      font-size: 31px;
    }

    @include screen-lg {
      font-size: 28px;
    }

  }

  p {
    font-family: "SSP";
    margin-top: 80px;
    font-size: 23px;
    font-weight: 100;
    line-height:1.6;
    width: 390px;
     @include screen-max(1850px) {
      font-size: 19px;
    }
    @include screen-max(1400px) {
      font-size: 17px;
      margin-top: 60px;
    }
    @include screen-lg {
      font-size: 16px;
      margin-top: 40px;
    }

    @include screen-sm {
      margin-top: 30px;
      width: auto;
    }
  }
}

.smart-yard-block__img {
  display: flex;
  margin-left: 20px;
  @include screen-xs {
    margin-top: 20px;
    justify-content: center;
  }
}

.smart-yard-block__img-mobile {
  width: 255px;
  height: 521px;
  background-position: center center;
  background-size: contain;
  background-repeat: no-repeat;
   @include screen-lg {
      width: 181px;
      height: 380px;
    }
  @include screen-xs {
    width: 181px;
    height: 210px;
  }
}

.smart-yard-block__img-yard-one {
    background-image: url(../assets/images/smartyardone.png);
      @include screen-sm {
      margin-right: 20px;
    }
}

.smart-yard-block__img-yard-two {
  margin: 50px 50px 0 50px;
    background-image: url(../assets/images/smartyardtwo.png);
     @include screen-md {
       display: none;
     }

     @include screen-xs {
       display: flex;
       margin: 30px 10px 0 20px;
     }
}
</style>
