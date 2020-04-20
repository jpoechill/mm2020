<template>
  <div>

    <div class="bg-blue pb-2">
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
            <button class="px-5 py-2 mt-3 button-on-dark rounded-0">
              <strong>
                REQUEST AN ESTIMATE 
              </strong> 
            </button>
          </div>
        </div>
      </div>
    </div>
    
    <div class="container mt-4">
      <div class="row">
        <div class="col-md-12 hidden" ref="hero" :class="{ 'fade-in' : showHero }">
          <img src="/cover.jpg" class="w-100" alt="">
        </div>
      </div>
    </div>
    <div class="container">
      <div class="row">
        <div class="col-md-6 mt-4 hidden" ref="goals" :class="{ 'fade-in' : showGoals }">
          <div class="p-4 border-top-blue pb-5 bg-white">
            <strong>OUR GOALS</strong><br><br>
            M&M is a commercial exterior building maintenance and service company. Our work includes everything from regular window and building cleaning, waterproofing, to historical restorations. <br><br>
            There is no building out of our reach, as we specialize in all types of aerial lift and suspension methods from bosuns chair work, boom lifts, scissor lifts, 2 point adjustable swing stage scaffolding, to the latest BMU rig operations. <br><br>
            Our skills and trade include: professional window washing, scratch glass removal, pressure washing, chemical cleaning, paint & protective coatings, building sealants, caulking & waterproofing. <br><br>
          </div>
        </div>
        <div class="col-md-6 mt-4 hidden" ref="work" :class="{ 'fade-in' : showWork }">
          <div class="p-4 pb-5 border-top-blue bg-white">
            <strong>OUR WORK</strong><br><br>
            With over 10 years in the building services business, M&M was established to compete with the toppling prices of the other companies in the industry. We are IICRC certified in water and fire damage restoration and can take on emergency projects across the country. <br><br>
            Our primary clients include major GC’s, property management companies, commercial real estate, building owners and facility maintenance management teams. <br><br>
            We bid on projects within 48 hrs and provide testing/mockups of the work being performed. We pride ourselves in being a one stop shop for all your buildings exterior needs.
          </div>
        </div>
      </div>
    </div>
    <div class="container mt-4 hidden" ref="servicesTopper" :class="{ 'fade-in' : showServices }">
      <div class="row">
        <div class="col-md-12">
          <div class="p-4 pb-3 border-top-blue bg-white">
            <strong>SERVICES</strong><br><br>
            <div class="container px-0">
              <div class="row">
                <div class="col-lg-4" v-for="(item, index) in allItems" v-bind:key="index">
                  <div class="tab mt-2 py-4 mb-4 bg-blue rounded text-center text-white text-uppercase">
                    <strong>
                      {{ item.name }}
                    </strong>
                  </div>
                  <div class="px-2 mb-4">
                    {{ item.description }}
                    <br><br><br>
                    <!-- Learn more. -->
                  </div>
                  <div class="px-2 pb-4 align-bottom text-secondary">
                    <br><br>
                    Learn more.
                  </div>
                </div>
              </div>
              <!-- <div class="row accordion" id="accordionExample2">
                <div class="col-md-3 pl-0">
                  <div>
                    <div class="" v-for="(item, index) in allItems" v-bind:key="index">
                      <div class="tab p-5 pb-5 mb-4 bg-blue rounded text-center text-white text-uppercase" id="headingOne" data-toggle="collapse" data-target="#collapseOne" aria-expanded="false" aria-controls="collapseOne">
                        <strong>
                          {{ item.name }}
                        </strong>
                      </div>
                      <div id="collapseOne" class="px-3 collapse" aria-labelledby="headingOne" data-parent="#accordionExample2">
                        <div class="mb-5">
                          {{ item.description }}
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div> -->
            </div>
          </div>
        </div>
      </div> 
    </div>
    <div class="container mt-4 hidden" ref="requestTopper" :class="{ 'fade-in' : showRequest }">
      <div class="row">
        <div class="col-md-12">
          <div class="p-4 pb-5 border-top-blue bg-white">
            <strong>REQUEST ESTIMATE</strong><br><br>
            <div class="container">
              <div class="row">
                <div class="pl-0 col-md-6">
                  Name
                  <div class="w-100">
                    <input type="text" class="w-100 input-text" name="" id="">
                  </div>
                </div>
                <div class="pr-0 col-md-6">
                  Email
                  <div class="w-100">
                    <input type="text" class="w-100 input-text" name="" id="">
                  </div>
                </div>
                <div class="col-md-12 mt-4 px-0">
                  Description
                  <textarea name="" id="" class="w-100" rows="10"></textarea>
                </div>
                <div class="col-md-12 mt-4 mb-2 px-0">
                  What is 2+2?
                  <div class="w-100">
                    <input type="text" class="w-100 input-text" name="" id="">
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
    <div class="container hidden" ref="contactTopper" :class="{ 'fade-in' : showContact }">
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
      items01: [
        {
          name: 'Building Cleaning',
          description: 'Final cleanings of new construction buildings to remove dirt and debris that happens during the construction.'
        }
      ],
      allItems: [
        {
          name: 'Building Cleaning',
          description: 'Final cleanings of new construction buildings to remove dirt and debris that happens during the construction.'
        },
        {
          name: 'Chemical Cleaning',
          description: 'Chemical building cleaning to remove efflorescence and calcium build up from the natural elements.'
        },
        {
          name: 'Solar Cleaning',
          description: 'Cleaning of solar panels to maximize efficiency of power to your grid, to maintain longevity, and to secure and maintain your investment.'
        },
        {
          name: 'Window Cleaning',
          description: 'Regular window cleaning for any size buildings, as well as construction glass cleaning to remove oxidation and water spots.'
        },
        {
          name: 'Anti-Graffiti',
          description: 'Anti graffiti coatings are typically applied to the lower elevations of buildings to protect from the damage of graffiti vandalism.'
        },
        {
          name: 'Paints & Coatings',
          description: 'Painting services to coat your property for a pleasant look aesthetically, and moreover, to protect your building with stronger coatings.'
        },
        {
          name: 'Building Sealants',
          description: 'We offer all types of weatherproofing on a case by case basis to help protect the needs of your building.'
        },
        {
          name: 'Weatherproofing',
          description: 'We provide industrial caulking services for all exterior facades and any size building. '
        },
        {
          name: 'Int. Dis. Fogging',
          description: 'Interior fogging to disinfect/ deodorize your office space, schools, and or any commercial properties. '
        }
      ],
      mouseX: 0,
      mouseY: 0,
      fadeElements: {
        showInfo: false,
        showGoals: false,
        showWork: false,
        showServices: false,
        showRequest: false,
        showContact: false
      },
      showHero: false,
      showInfo: false,
      showGoals: false,
      showWork: false,
      showServices: false,
      showRequest: false,
      showContact: false,
    }
  },
  methods: {
    submitRequest: function () {
      alert('Thank you for your estimate request, we will contact you shortly!')
    },
    handleScroll (currentY) {
      let prevScroll = this.scrollPos
      let currScroll

      console.log('Y: ' + typeof currentY)

      if (typeof currentY !== 'object') {
        currScroll = currentY
      } else {
        currScroll = window.scrollY
      }

      console.log(currScroll)
      console.log('Page height: ' + window.innerHeight)
      console.log('Y scroll: ' + window.scrollY)
      console.log('Sum: ' + (window.innerHeight + window.scrollY))
      // console.log(this.$refs.servicesTopper.offsetTop)

      let currBottomScroll = window.innerHeight + currScroll
      let servicesPos = this.$refs.servicesTopper.offsetTop
      let requestPos = this.$refs.requestTopper.offsetTop
      let contactPos = this.$refs.contactTopper.offsetTop
      let workPos = this.$refs.work.offsetTop
      let goalsPos = this.$refs.goals.offsetTop
      let heroPos = this.$refs.hero.offsetTop

      if (currBottomScroll >= (heroPos + 40)) {
        this.showHero = true
      }

      if (currBottomScroll >= (servicesPos + 40)) {
        this.showServices = true
      }

      if (currBottomScroll >= (requestPos + 40)) {
        this.showRequest = true
      }

      if (currBottomScroll >= (contactPos + 40)) {
        this.showContact = true
      }

      if (currBottomScroll >= (workPos + 40)) {
        this.showWork = true
      }

      if (currBottomScroll >= (goalsPos + 40)) {
        this.showGoals = true
      }
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
    },
    toggleHeight: function () {
      if (this.$refs.card1.style.height !== "300px") {
        this.$refs.card1.style.height = "300px"
      } else {
        this.$refs.card1.style.height = "152px"
      }
      
      this.showInfo = !this.showInfo
    }
  },
  mounted() { 
    this.handleScroll(window.scrollY)

    window.addEventListener('scroll', this.handleScroll);
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
  font-size: 18px;
  letter-spacing: 1px;;
}

.align-bottom {
  position: absolute;
  bottom: 0;
}

.input-text, textarea {
  border: none !important;
  background-color: #E7E7E7 !important;
  border-radius: 20px !important;
  padding: 10px !important;
  padding-left: 16px !important;
  margin-top: 10px !important;
  outline: none !important;
}

ul li {
  padding-right: 8px;
  font-size: 16px;
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

.show {
  display: block !important;
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
  transition: opacity 1s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}

.hidden {
  visibility: hidden;
  opacity: 0;
  transition: 1000ms ease-in-out;
  /* transform: translateX(-20px) */
}

.fade-in {
  visibility: visible;
  opacity: 1;
  /* transform: translateX(0px) */
}

.animate {
  height: 100px;
  -webkit-transition: all 1s ease;
  -moz-transition: all 1s ease;
  -o-transition: all 1s ease;
  -ms-transition: all 1s ease;
  transition: all 1s ease;
}
</style>
