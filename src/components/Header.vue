<template>
  <div>
    <div ref="header" class="item"></div>
  </div>
</template>

<script>
const classes = ['one', 'two', 'three']
export default {
  mounted () {
    this.addMedia()
  },
  methods: {
    addMedia () {
      let b = 0
      setInterval(() => {
        let item = this.$refs.header
        let classNameAdd = classes[b]
        item.classList.add(classNameAdd)
        if(b===0) {
        let classNameRemoveLenght = classes[classes.length-1]
        item.classList.remove(classNameRemoveLenght)

        }
        if(b>0) {
        let classNameRemove = classes[b-1]
        item.classList.remove(classNameRemove)
        }
        b++
        if(b===classes.length) {
          b=0
        }
      }, 5000)
    }
  }
}
</script>

<style>
.item {
  width: 50vw;
  height:50vw;
  margin:.5px;
  display:inline-block;
  background-position: center center;
  background-size: cover;
  background-repeat: no-repeat;
  background-image: url(../assets/images/donteco_tablet.png);
  transition: 1s;
  will-change: all;
}

.one {
  background-image: url(../assets/images/ugpa_slides.png);
}

.two {
  background-image: url(../assets/images/road.jpg);
}

.three {
  background-image: url(../assets/images/ugpa_tablet.png);
}


@keyframes bounce-in {
  0% {
    transform: scale(1);
  }

   70% {
    transform: scale(1.08);
  }

  100% {
    transform: scale(1.09);
  }
}

</style>
