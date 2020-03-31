<template>
  <div>
    <!-- <transition name="fade">
      <div ref="tooltip" class="mytooltip p-4 mb-4" v-if="showInfo">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Placeat velit minima sed laudantium porro voluptatem saepe dolores fugit, veniam tempora dolorum obcaecati nobis aut asperiores. Impedit eveniet excepturi illum rerum.
      </div>
    </transition> -->

    <div class="bg-blue pb-1">
      <div class="container">
        <div class="row">
          <div class="col-md-7 pt-4 text-white text-uppercase">
            <span class="logo-text font-weight-bold mr-5">M&M</span> 
            <ul class="list-inline d-inline">
              <li class="list-inline-item">About</li>
              <li class="list-inline-item">Services</li>
              <li class="list-inline-item">Contact</li>
            </ul>  
          </div>
          <div class="col-md-5 py-4 text-right text-white">
            <button class="px-5 py-1 mt-1 button-on-dark rounded-0">
              <strong>
                REQUEST ESTIMATE 
              </strong> 
            </button>
          </div>
        </div>
      </div>
    </div>
    <div class="container mt-4">
      <div class="row">
        <div class="col-md-12">
          <img src="/cover.jpg" class="w-100" alt="">
        </div>
      </div>
    </div>
    <div class="container">
      <div class="row">
        <div class="col-md-6 mt-4">
          <div class="p-4 border-top-blue pb-5 bg-white">
            <strong>OUR GOALS</strong><br><br>
            M&M is a commercial exterior building maintenance and service company. Our work includes everything from regular window and building cleaning, waterproofing, to historical restorations. There is no building out of our reach, as we specialize in all types of aerial lift and suspension methods from bosuns chair work, boom lifts, scissor lifts, 2 point adjustable swing stage scaffolding, to the latest BMU rig operations. Our skills and trade include: professional window washing, scratch glass removal, pressure washing, chemical cleaning, paint & protective coatings, building sealants, caulking & waterproofing.
          </div>
        </div>
        <div class="col-md-6 mt-4">
          <div class="p-4 pb-5 border-top-blue bg-white">
            <strong>OUR WORK</strong><br><br>
            With over 10 years in the building services business, M&M was established to compete with the toppling prices of the other companies in the industry. We are IICRC certified in water and fire damage restoration and can take on emergency projects across the country. Our primary clients include major GC’s, property management companies, commercial real estate, building owners and facility maintenance management teams. We bid on projects within 48 hrs and provide testing/mockups of the work being performed. We pride ourselves in being a one stop shop for all your buildings exterior needs.
          </div>
        </div>
      </div>
    </div>
    <div class="container mt-4">
      <div class="row">
        <div class="col-md-12">
          <div class="p-4 pb-5 border-top-blue bg-white">
            <strong>SERVICES</strong><br><br>
            <div class="container">
              <div class="row">
                <div class="col-md-6 pl-0">
                  <div class="tab p-5 pb-5 mb-4 bg-blue rounded text-center text-white" @click="toggleCard()" @mousemove="readMousePos" @mouseenter="showInfo = true;" @mouseleave="showInfo = false;">
                    <strong>
                      INT. DISINFECTANT FOGGING
                    </strong>
                  </div>
                </div>
                <!-- <div class="col-md-6 pl-0">
                  <div class="p-5 pb-5 mb-4 bg-blue rounded text-center text-white" @mousemove="readMousePos" @mouseenter="showInfo = true" @mouseout="showInfo = false">
                    <strong>INT. DISINFECTANT FOGGING</strong>
                  </div>
                  <div class="px-4 mb-4" v-show="showInfo">
                    Lorem ipsum dolor sit amet, consectetur adipisicing elit. Placeat velit minima sed laudantium porro voluptatem saepe dolores fugit, veniam tempora dolorum obcaecati nobis aut asperiores. Impedit eveniet excepturi illum rerum.
                  </div>
                </div> -->
                <div class="col-md-6 pr-0">
                  <div class="tab p-5 pb-5 mb-4 bg-blue rounded text-center text-white" @click="toggleCard()" >
                    <strong>SOLAR PANELS</strong>
                  </div>
                </div>
                <div class="col-md-6 pl-0">
                  <div class="tab p-5 pb-5 mb-4 bg-blue rounded text-center text-white" @click="toggleCard()" >
                    <strong>WATER PROOFING</strong>
                  </div>
                </div>
                <div class="col-md-6 pr-0">
                  <div class="tab p-5 pb-5 mb-4 bg-blue rounded text-center text-white" @click="toggleCard()" >
                    <strong>WINDOW CLEANING</strong>
                  </div>
                </div>
                <div class="col-md-6 pl-0">
                  <div class="tab p-5 pb-5 bg-blue rounded text-center text-white" @click="toggleCard()" >
                    <strong>BUILDING RESTORATION</strong>
                  </div>
                </div>
                <!-- <div class="col-md-6 pl-0">
                  {{ mouseX }} <br>
                  {{ mouseY }}
                </div> -->
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="container mt-4">
      <div class="row">
        <div class="col-md-12">
          <div class="p-4 pb-5 border-top-blue bg-white">
            <strong>REQUEST ESTIMATE</strong><br><br>
            <div class="container">
              <div class="row">
                <div class="pl-0 col-md-6">
                  Name
                  <div class="w-100">
                    <input type="text" class="w-100" name="" id="">
                  </div>
                </div>
                <div class="pr-0 col-md-6">
                  Email
                  <div class="w-100">
                    <input type="text" class="w-100" name="" id="">
                  </div>
                </div>
                <div class="col-md-12 mt-4 px-0">
                  Description
                  <textarea name="" id="" class="w-100" rows="10"></textarea>
                </div>
                <div class="col-md-12 mt-4 mb-2 px-0">
                  What is 2+2?
                  <div class="w-100">
                    <input type="text" class="w-100" name="" id="">
                  </div>
                </div>
                <div class="col-md-12 mt-4 text-center">
                  <button class="px-5 py-2 button-on-white text-white" @click="submitRequest()">
                    <strong>
                      REQUEST ESTIMATE
                    </strong>
                  </button>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="container">
      <div class="row">
        <div class="col-md-12 mt-4">
          <div class="p-4 pb-5 border-top-blue bg-white">
            <strong>CONTACT</strong><br><br>
            Support may be available directly at 619-917-7029, or by email via. hello@mmbuildingservices.com.
          </div>
        </div>
      </div>
    </div>
    <div class="container my-5">
      <div class="row">
        <div class="col-md-12 text-center">
          M&M Building Services © 2020
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      mouseX: 0,
      mouseY: 0,
      showInfo: false
    }
  },
  methods: {
    submitRequest: function () {
      alert('Thank you for your estimate request, we will contact you shortly!')
    },
    readMousePos: function (event) {
      // if (this.showInfo) {
      //    this.mouseX = event.offsetX
      //   this.mouseY = event.offsetY
      //   // this.mouseX = event.pageX
      //   // this.mouseY = event.pageY
      //   console.log(event)

      //   // console.log(this.$refs.tooltip)
      //   if (this.$refs.tooltip.style) {
      //     this.$refs.tooltip.style.top = event.pageY - 8 + 'px'
      //     this.$refs.tooltip.style.left = event.pageX + 26 + 'px'
      //   }
      // }
    },
    toggleCard: function () {
      alert('You clicked me!')
    }
  },
  mounted() {
    // console.log(window)
    // document.addEventListener('mousemove', this.readMousePos, false);
    // console.log(document)    
  },
}
</script>

<style>
body, html {
  background-color: #eee;
}

.logo-text {
  font-size: 33px !important;
  border-bottom: 5px solid #FFF;
}

.bg-blue {
  background-color: #0D101E;
}

.mw-none {
  max-width: none;
}

.border-top-blue {
  border-top: 10px solid #0D101E;
}

strong {
  font-size: 24px;
  letter-spacing: 1px;;
}

input[type="text"], textarea {
  border: none;
  background-color: #E7E7E7;
  border-radius: 20px;
  padding: 10px;
  padding-left: 16px;
  margin-top: 10px;
  outline: none;
}

ul li {
  padding-right: 8px;
  font-size: 20px;
  letter-spacing: 1px;
}

.button-on-white {
  background-color: #0D101E;
  border-radius: 10px;
}

.button-on-dark {
  background-color: #FFFFFF;
  border: none;
  color: #0D101E;
  border-radius: 10px;
}

button:hover, .tab {
  cursor: pointer;
}

/* .tooltip-wrapper:hover .tooltip {
  display: block;
} */

.mytooltip {
  /* display: block; */
  background-color: white;
  position: absolute;
  z-index: 1000;
  border-radius: 10px;
  width: 500px;
  /* height: 300px; */
  transition: opacity .25s ease-in-out;
  /* top: 40px;
  left: 40px; */
  box-shadow: 4px 4px 10px 2px rgba(0, 0, 0, .30);
}

.fade-enter-active, .fade-leave-active {
  transition: opacity .5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>
