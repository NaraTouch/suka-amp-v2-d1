<template>
 <section>
   <div class="page-container">
     <!-- header -->
      <header class="page-header">
        <nav-bar-header />
      </header>

        <!-- body -->
      <div class="body-container">
        <!-- running-text -->
        <div>
          <running-text />
        </div>
        <!-- nav-bar-image -->

        <div class="navbar-header">
          <nav-image />
        </div>

        <!-- running-image -->
        <div class="running-image-header">
          <running-image />
        </div>

        <!-- body -->
        <div class="body-field">
          <section class="row-left">
            <!-- tab-winner -->
            <div class="tab-winner">
              <tab-winner />
            </div>

            <!-- slider-promotion -->
            <div class="slider-promotion">
              <slider :slide-list="sliderPromotion" :slider="slderCondition" />
            </div>
            <!-- stay-connected -->
            <div class="stay-connected">
              <stay-connected />
            </div>

            <!-- payment-method -->
            <div class="payment-method">
              <payment-method />
            </div>
            <!-- contect-text -->
            <div class="content-text">
               <content-text />
            </div>
          </section>

          <article class="row-right">
            <!-- slider-image -->
            <div class="slider-image">
              <slider :slide-list="sliderImage" />
              <slider-path />
            </div>

            <div class="card-content">
              <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Enim voluptas alias possimus libero, totam, necessitatibus cum quo molestias perferendis reiciendis expedita impedit facilis quae. Tenetur magnam cupiditate natus suscipit nemo.</p>
            </div>
          </article>
        </div>

      </div>

      <!-- footer -->
      <footer>

      </footer>
   </div>
 </section>
</template>

<script>
  export default {
    components: {
      NavBarHeader: () => import('../components/header/NavBarHeader'),
      RunningText: () => import('../components/RunningText'),
      NavImage: () => import("../components/body/NavImage"),
      RunningImage: () => import("../components/RunningImage"),
      TabWinner: () => import("../components/Tab/TabWinner"),
      Slider: () => import("../components/slider/Slider"),
      SliderPath: () => import("../components/slider/SliderPath"),
      PaymentMethod: () => import("../components/Payment/PaymentMethod"),
      ContentText: () => import("../components/content/ContentText"),
    },
    data() {
      return {
        count: 0,
        src: "../static/images/images.jpg",
        sliderPromotion: "/data/slider-list.json",
        sliderImage: "/data/slider-image-list.json",
        slderCondition: true, 
      };
    },
  }
</script>

<style lang="scss">
  .page-container {
    .body-container {
      @extend .container-size;
      margin: 0 auto;
      padding: 10px 0px;
    }
    .navbar-header {
      padding: 10px 0px;
    }
    .running-image-header {
      padding: 6px 0px 0px 0px;
    }
    .body-field {
      display: flex;
      margin-top: 10px;

      .row-left {
        min-width: 265px;
        background: burlywood;
        padding-right: 15px;

        .tab-winner {
          
        }
        .slider-promotion {
          @extend .mr-box;
        }
        .stay-connected {
          margin-bottom: 30px;
          background-color: $bg-body-field;
          @extend .border-radius-5px;
        }
        .payment-method {
          padding-bottom: 5px;
          @extend .border-radius-5px;
          background-color: $bg-body-field;
        }
        .content-text {
            margin-top: 20px;
        }
      }
      .row-right {
        min-width: 760px;
        background: yellowgreen;
        padding-left: 15px;

        .slider-image {
          background-color: $bg-body-field;
        }
        .card-content {
          padding: 10px 0px 0px 0px;
        }
      }
    }
  }
</style>