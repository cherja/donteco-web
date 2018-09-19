<template>
  <div class="company-staff-block container">
    <div class="company-staff-block__image-mobile">
      <div class="company-staff-block__stickers-seagullblue"/>
    </div>
    <div class="company-staff-block__text">
      <div class="company-staff-block__stickers-circlered"/>
      <div class="company-staff-block__stickers-crossdarkblue"/>
      <p>8 WEB-РАЗРАБОТЧИКОВ</p><br>
      <p>6 MOBILE-РАЗРАБОТЧИКОВ</p><br>
      <p>2 ДИЗАЙНЕРА ИНТЕРФЕЙСОВ</p><br>
      <p>2 ПРОЕКТНЫХ МЕНЕДЖЕРА</p><br>
      <p>1 QA СПЕЦИАЛИСТ</p>
    </div>
    <div class="company-staff-block__image">
      <div class="company-staff-block__stickers-rectanglegreen"/>
    </div>
  </div>
</template>

<style lang="scss">
@import "../helpers";

.company-staff-block {
  display: flex;
  justify-content: space-between;
  margin-bottom: 100px;
   @include screen-sm {
      display:block;
    }
}

.company-staff-block__image {
  position: relative;
  margin-right: 110px;
  background-position: center center;
  background-size: contain;
  background-repeat: no-repeat;
  background-image: url(../assets/images/companystaff.png);
  width: 500px;
  height: 350px;
  @include screen-lg {
      width: 400px;
      height: 250px;
    }
     @include screen-md {
      width: 350px;
      height: 220px;
      margin-right: 50px;
    }
    @include screen-sm {
      display:none;
    }
}

.company-staff-block__image-mobile {
  display: none;
  @include screen-sm {
      width: 400px;
      height: 250px;
      position: relative;
      margin-right: 110px;
      background-position: center center;
      background-size: contain;
      background-repeat: no-repeat;
      background-image: url(../assets/images/companystaff.png);
      display: block;
      margin-left: auto;
      margin-right: 0em;
    }
    @include screen-xs {
      width: 320px;
      margin: auto;
      margin-bottom: 30px;
    }
}

.company-staff-block__stickers-seagullblue {
  width: 70px;
  height: 50px;
  position: absolute;
  background-position: center center;
  background-size: contain;
  background-repeat: no-repeat;
  background-image: url(../assets/images/seagullblue.png);
  left: -30px;
}
.company-staff-block__text {
  color: #22c3ba;
  font-size: 60px;
  position: relative;
  margin-top: 80px;
  line-height: 1.5;
  @include screen-max(1850px) {
      font-size: 45px;
    }

    @include screen-max(1400px) {
      font-size: 35px;
    }

    @include screen-lg {
      font-size: 30px;
    }
    @include screen-md {
      font-size: 25px;
    }
    @include screen-xs {
      width: 320px;
      margin: auto;
    }
    p {
      font-family: "BNB";
      letter-spacing: 1px;
      border-bottom: 2px solid #22c3ba;
      font-weight: 600;
      display: inline-block;
    }
}

 .company-staff-block__stickers-circlered {
  width: 50px;
  height: 50px;
  position: absolute;
  background-position: center center;
  background-size: contain;
  background-repeat: no-repeat;
  background-image: url(../assets/images/circlered.png);
  right: -100px;
    @include screen-sm {
      right: 100px;
    }
    @include screen-xs {
      top: -30px;
      right:0px;
    }
 }

 .company-staff-block__stickers-crossdarkblue {
  width: 70px;
  height: 70px;
  position: absolute;
  background-position: center center;
  background-size: contain;
  background-repeat: no-repeat;
  background-image: url(../assets/images/crossdarkblue.png);
  bottom: 30px;
  right: -350px;
   @include screen-max(1750px) {
       width: 60px;
       height: 60px;
       bottom: -30px;
       right: 0px;
    }
    @include screen-sm {
      right: 300px;
    }
    @include screen-xs {
      bottom: -50px;
    }
 }

 .company-staff-block__stickers-rectanglegreen {
  width: 90px;
  height: 20px;
  position: absolute;
  background-position: center center;
  background-size: contain;
  background-repeat: no-repeat;
  background-image: url(../assets/images/rectanglegreen.png);
  bottom: -50px;
    @include screen-max(1850px) {
  width: 70px;
    }
 }

</style>
