<template>
  <section >
    <div class="grid-body">
      <header class="page-header">
        <nav-bar-header />
      </header>
      
      <div class="container container-content container-wide">
        <!-- header -->
        <div class="running-text-header">
          <running-text />
        </div>

        <nav class="navbar-header">
          <nav-image /> 
        </nav>

        <div class="running-image-header">
          <running-image />
        </div>

        <!-- left-box -->
         <div class="box tab-winner-left">
          <tab-winner />
        </div>

        <div class="box slider-promotion-left">
          <Slider :slide-list="sliderPromotion" :slider="slderCondition" />
        </div>

        <div class="box stay-connected-left">
            <stay-connected />
        </div>

        <div class="box payment-methods-left">
          <payment-method />
        </div>

        <div class="box footer-text-left">
          <content-text />
        </div> 
        
        <!-- right-box -->
         <div class="box carousel-slide">
          <Slider :slide-list="sliderImage" />
          <SliderPath />
        </div>

        <div class="box card">
          <h2>seven</h2>
        </div> 

        <!-- footer -->
        <div class="box footer">
          <h2>eight</h2>
        </div>
      
      </div>

    </div>
  </section> 
</template>

<script>
export default {
  components: {
    NavBarHeader: () => import('../components/header/NavBarHeader'),
    RunningText: () => import('../components/RunningText'),
    NavImage: () => import('../components/body/NavImage'),
    RunningImage: () => import('../components/RunningImage'),
    TabWinner: () => import('../components/Tab/TabWinner'),
    Slider: () => import('../components/slider/Slider'),
    TabWinner: () => import('../components/Tab/TabWinner'),
    StayConnected: () => import('../components/stay-connected/StayConnected'),
    PaymentMethod: () => import('../components/Payment/PaymentMethod'),
    ContentText: () => import('../components/content/ContentText'),
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
}
</script>

<style lang="scss">
  .grid-body {
    .container {
      display: grid;
      background: blue;
      // padding: 1em 5em;
      grid-gap: 0.5em;
      border-bottom: 5px solid darkblue;
        border-top: 5px solid darkblue;
      grid-template-areas: 
      'running-text running-text running-text running-text running-text'
      'navbar navbar navbar navbar navbar'
      'running-image running-image running-image running-image running-image'
      'tab-winner carousel-slide carousel-slide carousel-slide carousel-slide'
      'slider-promotion card card card card'
      'stay-connected card card card card'
      'payment-methods card card card card'
      'footer-text card card card card'
      'footer footer footer footer footer';
      grid-template-columns: 25% 1fr;

     .running-image-header,.running-text-header , .stay-connected-left, .payment-methods-left, .footer-text-left, .card, .footer {
        background-color: aqua;
      }
       .container-wide {
        margin-left: auto;
        margin-right: auto;
      }
      .box {
        // padding: 3em;
        // text-align: center;
        // transition: all .1s linear;
        // background: white;
      }

      // header 
      .running-text-header {
        grid-area: running-text;
      }
      .navbar-header {
        grid-area: navbar;
      }
      .running-image-header {
        grid-area: running-image;
      }

      // left
      .tab-winner-left {
        grid-area: tab-winner;
        height: 400px;
      }
      .slider-promotion-left {
        grid-area: slider-promotion;
        height: 360px;
      }
      .stay-connected-left {
        grid-area: stay-connected;
      }
      .payment-methods-left {
        grid-area: payment-methods;
        height: 285px;
      }
      .footer-text-left {
        grid-area: footer-text;
      }

      // right 
      .carousel-slide{ 
        grid-area: carousel-slide;
        height: 340px;
        background-image: url(/images/header/header-announcement-back.png);
      }
      .card {
        grid-area: card;
        margin-top: -60px;
      }
      
      // footer
      .footer {
        grid-area: footer;
      }

    }
  }
</style>