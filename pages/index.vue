<template>
  <section>
    <div class="home-page">
      <!-- NavBar  -->
      <div>
          <NavBarHeader />
      </div>
      
      <!-- Container -->
      <div class="display-container container-content container-wide">
        <!-- Header -->
          <div class="running-text">
            <RunningText />
          </div>

          <div class="header-text">
            <NavImage />
          </div>

          <div class="running-image">
            <RunningImage />
          </div>

        <!-- Body -->
        <!-- col-left -->
        <div class="tab-winner">
          <TabWinner />
        </div>

        <div class="slider-promotion"> 
          <Slider :slide-list="sliderPromotion" :slider="slderCondition" />
        </div>

        <div class="stay-connected">
          <StayConnected />
        </div>
        
        <div class="payment-method">
          <PaymentMethod />
        </div>

        <div class="content-text">
          <ContentText />
        </div>

        <!-- Body -->
        <!-- col-right -->
        <div class="slider-image">
          <!-- <Test /> -->
             <Slider :slide-list="sliderImage" />
             <SliderPath /> 
        </div>

      </div>

      <!-- Footer -->
      <div>

      </div>
    </div>
  </section>
</template>

<script>
export default {
  components: {
    Navigation: () => import('../components/Navigation'),
    RunningImage: () => import('../components/RunningImage'),
    MultipleCarousel: () => import('../components/MultipleCarousel'),
    NavBarHeader: () => import('../components/header/NavBarHeader'),
    RunningText: () => import('../components/RunningText'),
    NavImage: () => import('../components/body/NavImage'),
    TabWinner: () => import('../components/Tab/TabWinner'),
    Slider: () => import('../components/slider/Slider'),
    StayConnected: () => import('../components/stay-connected/StayConnected'),
    ContentText: () => import('../components/content/ContentText'),
    SliderPath: () => import('../components/slider/SliderPath'),
    PaymentMethod: () => import('../components/Payment/PaymentMethod'),
    
  },
  data() {
    return {
        count: 0,
        src: "../static/images/images.jpg",
        sliderPromotion: "/data/slider-list.json",
        sliderImage: "/data/slider-image-list.json",
        slderCondition: true,
    }
  },
  methods: {
    say: function (message) {
      alert(message)
    }
  },
  watch: {
     say: function (count) {
      alert(this.count)
    }
  },
}
</script>


<style lang="scss" scoped>
  .home-page {
    // Navbar-Header
    
    // Container-style
    .display-container {
      margin-top: 10px;
      display: grid;        
      grid-template-columns: repeat(4, 1fr); 
      grid-template-rows: 0.1fr 0.2fr 0.1fr 1.2fr;
      grid-template-areas:
      "running-text running-text running-text running-text"
      "header-text header-text header-text header-text"
      "running-image running-image running-image running-image"
      "tab-winner slider-image slider-image slider-image"
      "slider-promotion slider-image slider-image slider-image"
      "stay-connected slider-image slider-image slider-image"
      "payment-method slider-image slider-image slider-image"
      "content-text sidebar-right sidebar-right sidebar-right";
      // "footer footer footer footer";
      gap: 0.5rem;
      height: 100vh;
      font-weight: 800;
      font-size: 12px;
      color: $color-white;
      text-align: center;
    }
    .container-content {
      max-width: 1500px;
    }
    .container-wide {
      margin-left: auto;
      margin-right: auto;
    }
    // cloumn
    //left
    .running-text {
      grid-area: running-text;
    }
    .header-text {
      grid-area: header-text;
    }
    .running-image {
      grid-area: running-image;
    }
    .tab-winner {
       grid-area: tab-winner;
    }
    .slider-promotion {
      grid-area: slider-promotion;
    }
    .stay-connected {
      grid-area: stay-connected;
      background-color: $color-gray;
      @extend .border-radius-5px;
    }
    .payment-method {
      grid-area: payment-method;
      background-color: $color-gray;
    }
    .content-text {
      grid-area: content-text;
    }

    // right
    .slider-image {
       grid-area: slider-image;
    }
  }
</style>
