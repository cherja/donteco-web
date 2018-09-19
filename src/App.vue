<template>
  <div id="app" class="wrapper">
    <modalcontent
      v-if="isShow"
      @close="isShow = false"
    />
    <headercomponent @open="isShow = true"/>
    <ugpa/>
    <gobambino/>
    <donteco/>
    <aboutcompany/>
    <companystaff/>
    <forminlayout/>
    <companyaddress/>
    <footerblock/>
  </div>
</template>

<script>
import headercomponent from './components/Header.vue'
import ugpa from './components/Ugpa.vue'
import gobambino from './components/Gobambino.vue'
import donteco from './components/Donteco.vue'
import aboutcompany from './components/AboutCompany.vue'
import companystaff from './components/CompanyStaff.vue'
import forminlayout from './components/FormInLayout.vue'
import companyaddress from './components/CompanyAddress.vue'
import footerblock from './components/Footer.vue'
import modalcontent from './components/Modal.vue'

export default {
  components: {
    headercomponent,
    ugpa,
    gobambino,
    donteco,
    aboutcompany,
    companystaff,
    forminlayout,
    companyaddress,
    footerblock,
    modalcontent
  },
  name: 'app',
  data () {
    return {
      isShow: false
    }
  }
}
</script>

<style lang="scss">
@import "./helpers";

@font-face {
  font-family: "BBB";
  src: url("./assets/fonts/bebasbeuebold.otf");
}

@font-face {
  font-family: "SSP";
  src: url("./assets/fonts/sourcesanspro.ttf");
}

@font-face {
  font-family: "BNB";
  src: url("./assets/fonts/bebasneuebook.ttf");
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.wrapper {
  max-width: 2000px;
  margin: auto;
  overflow: hidden;
}

.container {
  padding: 0 50px 0 320px;

   @include screen-max(1600px) {
      padding: 0 50px 0 200px;
    }

   @include screen-max(1400px) {
      padding: 0 50px 0 100px;
    }

    @include screen-md {
     padding: 0 0 0 50px;
    }

    @include screen-xs {
    padding: 0px;
  }
}

.container-center {
  margin:auto;
  padding: 0 320px;

   @include screen-max(1600px) {
      padding: 0 200px;
    }

   @include screen-max(1400px) {
      padding: 0 100px;
    }

    @include screen-md {
     padding: 0 50px;
    }

    @include screen-xs {
    padding: 0px;
  }
}

.all-project-block {
  padding: 10vw 8vw 0 8vw;
  font-family: "BNB";
  justify-content: space-between;
  font-size: 3.5vw;
  color: white;
  letter-spacing: 1px;
  font-weight: 600;
  display: flex;
  @include screen-sm {
    flex-direction: column-reverse;
    align-items: center;
  }
}

.slides_text>p {
  @include screen-sm {
   display: none;
  }
}

.tablet_text>p {
  display: none;
  @include screen-sm {
   display: block;
   text-align: center;
   font-size: 4.5vw;
  }
}

.all-tablet {
  width: 37vw;
  height: 30vw;
  background-position: center center;
  background-size: contain;
  background-repeat: no-repeat;
  @include screen-sm {
    width: 70vw;
    height: 67vw;
  }
}
.all-slides {
  width: 35vw;
  height: 33vw;
  background-position: center center;
  background-size: contain;
  background-repeat: no-repeat;
  @include screen-sm {
    width: 70vw;
    height: 65vw;
  }
}
</style>
