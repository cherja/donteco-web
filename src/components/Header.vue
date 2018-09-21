<template>
  <div>
    <div class="frame">
      <div v-show="a" class="item a">
        <div class="one-block-little-img">
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
      <div v-show="b" class="item b">
        <div class="one-block-little-img">
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
      <div v-show="c" class="item c">
        <div class="one-block-little-img">
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

<script>
export default {
  data () {
    return {
      a: false,
      b: false,
      c: false
    }
  },
  mounted () {
    this.addMedia()
  },
  methods: {
    addMedia () {
      let i = 0
      setInterval(() => {
        if (i === 3) {
          this.c = false
          this.a = true
          i = 1
          return
        }
        if (i === 0) {
          this.a = true
        }
        if (i === 1) {
          this.a = false
          this.b = true
        }
        if (i === 2) {
          this.b = false
          this.c = true
        }
        i++
      }, 7000)
    }
  }
}

</script>

<style>
.frame {
  width: 80vw;
  height:50vw;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
  margin: auto;
}
.item {
  display: flex;
  justify-content: space-between;
  width: 80vw;
  height:40vw;
  background-position: center center;
  background-size: cover;
  background-repeat: no-repeat;
  transition: transform 2s ease;
  will-change: transform;
  position: relative;
  left: -80vw;
}

.a {
  animation: scale-cover 5s;
  background-image: url(../assets/images/1.jpg);
}
.b {
  animation: scale-cover 5s;
  background-image: url(../assets/images/2.jpg);
}
.c {
  animation: scale-cover 5s;
  background-image: url(../assets/images/3.png);
}
.zero {
  background-position: center center;
  background-size: cover;
  background-repeat: no-repeat;
}

.one-block-little-img {
  position: relative;
  left: -20vw;
  animation: one 5s;
}

.one {
background-image: url(../assets/images/4.jpg);
width: 20vw;
height:25vw;
}
.two {
width: 20vw;
height:15vw;
background-image: url(../assets/images/5.jpg);
}
.three {
width: 20vw;
height:15vw;
background-image: url(../assets/images/6.jpg);
}
.four {
width: 20vw;
height:25vw;
background-image: url(../assets/images/7.png);
}
.five {
width: 20vw;
height:25vw;
background-image: url(../assets/images/8.png);
}
.six {
width: 20vw;
height:15vw;
}
.seven {
width: 20vw;
height:25vw;
}
.eight {
width: 20vw;
height:15vw;
background-image: url(../assets/images/road.jpg);
}

@keyframes scale-cover {
  0% {
    transform: translateX(0vw);
  }
  10% {
    transform: translateX(80vw);
  }
  90% {
    transform: translateX(80vw);
  }
  100% {
    transform: translateX(0vw);
  }
}
@keyframes one {
  0% {
    transform: translateX(0vw);
  }
  8% {
    transform: translateX(0vw);
  }
  30% {
    transform: translateX(20vw);
  }
  80% {
    transform: translateX(20vw);
  }
  100% {
    transform: translateX(0vw);
  }
}

</style>
