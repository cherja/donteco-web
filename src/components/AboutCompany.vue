<template>
  <div class="container">
    <div class="about-company-block">
    <div class="about-company-block__text">
      <div class="about-company-block__stickers about-company-block__stickers-circleblue"/>
      <div class="about-company-block__stickers about-company-block__stickers-circlegrey"/>
      <div class="about-company-block__stickers about-company-block__stickers-crossred"/>
      <div class="about-company-block__stickers about-company-block__stickers-circledarkblue"/>
      <div class="about-company-block__stickers about-company-block__stickers-seagullblue"/>
      <div class="about-company-block__stickers about-company-block__stickers-seagullblue-lg"/>
      <div class="about-company-block__stickers about-company-block__stickers-seagullred"/>
      <div class="about-company-block__stickers about-company-block__stickers-circlebluebtn"/>
      <div class="about-company-block__stickers about-company-block__stickers-rectangledarkblue"/>
      <div class="about-company-block__stickers about-company-block__stickers-crossblue"/>
      <div class="about-company-block__stickers about-company-block__stickers-crossdarkblue"/>
      <div class="about-company-block__stickers about-company-block__stickers-rectangleblue"/>
      <p>
        Компания Donteco - коллектив разработчиков и дизайнеров, собранный из лучших выпускников престижных ВУЗов Ростова-на-Дону. Широкий спектр специализации нашей команды позволяет решать задачи любой сложности, начиная от создания игр виртуальной реальности, заканчивая сложнейшими интеграциями. Нас отличает высокая прозрачность процесса производства - начиная от детального расчета смет и заканчивая последующим внедрением и обслуживанием системы
      </p>
      <p>
        Если у Вас сложный технологический проект - мы реализуем его качественно, прозрачно и в установленные сроки
      </p>
    </div>
    </div>
  </div>
</template>

<style lang="scss">
@import "../helpers";

.about-company-block {
  display: flex;
  justify-content: flex-end;
}

.about-company-block__text {
  margin: 200px 180px 300px 0;
  width: 850px;
  background: linear-gradient(to right, #3675ec, #7088f6);
  border: 1px solid #3875ec;
    position: relative;
    @include screen-max(1500px) {
      margin: 100px 100px 200px 0;
      width: 700px;
    }
     @include screen-sm {
      margin: 50px 20px 50px 0;
      width: 100%;
    }
     @include screen-xs {
      margin: 50px 0 50px 0;
    }

  p {
    color: white;
    font-size: 20px;
    font-weight: 100;
    letter-spacing: 1px;
    line-height:1.6;
    margin: 50px;
    font-family: "SSP";
    @include screen-max(1400px) {
      font-size: 18px;
      margin-top: 60px;
    }
    @include screen-lg {
      font-size: 16px;
      margin-top: 40px;
    }

    @include screen-sm {
      margin-top: 30px;
      font-size: 14px;
    }
     @include screen-xs {
      margin: 30px;
    }
  }
}

.about-company-block__stickers {
  width: 60px;
  height: 60px;
  position: absolute;
  background-position: center center;
  background-size: contain;
  background-repeat: no-repeat;
}

.about-company-block__stickers-circleblue {
  background-image: url(../assets/images/circleblue.png);
   z-index: -1;
  top:-180px;
  left: -550px;
   @include screen-sm {
     display: none;
    }
}

.about-company-block__stickers-circlegrey {
  background-image: url(../assets/images/circlegrey.png);
  top:-60px;
  left: -150px;
   @include screen-sm {
     display: none;
    }
}

.about-company-block__stickers-crossred {
  background-image: url(../assets/images/crossred.png);
  top:60px;
  left: -350px;
  @include screen-sm {
     display: none;
    }
}

.about-company-block__stickers-circledarkblue {
  background-image: url(../assets/images/circledarkblue.png);
  bottom: 0px;
  left: -350px;
  @include screen-sm {
     display: none;
    }
}

.about-company-block__stickers-seagullblue {
  background-image: url(../assets/images/seagullblue.png);
  bottom: 250px;
  left: -700px;
  @include screen-sm {
     display: none;
    }
}

.about-company-block__stickers-seagullblue-lg {
  background-image: url(../assets/images/seagullblue.png);
  width: 100px;
  height: 80px;
  bottom: -250px;
  left: -700px;
  @include screen-sm {
     display: none;
    }
}

.about-company-block__stickers-seagullred {
  background-image: url(../assets/images/seagullred.png);
  width: 80px;
  height: 80px;
  bottom: -200px;
   @include screen-sm {
     top: -40px;
     left: 30px;
    }
}

.about-company-block__stickers-circlebluebtn {
  background-image: url(../assets/images/circleblue.png);
  height: 40px;
  bottom: -150px;
  left: 300px;
  @include screen-sm {
     display: none;
    }
}

.about-company-block__stickers-rectangledarkblue {
  background-image: url(../assets/images/rectangledarkblue.png);
  bottom:-200px;
  right: 150px;
  @include screen-sm {
     display: none;
    }
}

.about-company-block__stickers-crossblue {
  background-image: url(../assets/images/crossblue.png);
  bottom:200px;
  right: -30px;
}

.about-company-block__stickers-crossdarkblue {
  background-image: url(../assets/images/crossdarkblue.png);
  bottom:-55px;
  left: 90px;
  @include screen-sm {
     display: none;
    }
}

.about-company-block__stickers-rectangleblue {
  background-image: url(../assets/images/rectangleblue.png);
  bottom:150px;
  left: -100px;
  @include screen-sm {
     display: none;
    }
}

</style>
