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

            <div class="border-row">
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
              <card-game />
            </div>
            
           
          </article>
        </div>

        <!-- footer -->
        <div class="page-footer">
          <footer-page />
        </div>

         <!-- Action-component -->
        <div class="action-component">
          <action-connection />
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
      NavImage: () => import("../components/body/NavImage"),
      RunningImage: () => import('../components/RunningImage'),
      TabWinner: () => import('../components/Tab/TabWinner'),
      Slider: () => import('../components/slider/Slider'),
      SliderPath: () => import('../components/slider/SliderPath'),
      PaymentMethod: () => import('../components/Payment/PaymentMethod'),
      ContentText: () => import('../components/content/ContentText'),
      CardGame: () => import('../components/card/CardGame'),
      FooterPage: () => import('../components/FooterPage'),
      ActionConnection: () => import('../components/action/ActionConnection'),
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

      .navbar-header {
        padding: 10px 0px;
      }

      .running-image-header {
        padding: 6px 0px 0px 0px;
      }

      .body-field {
        display: flex;
        margin: 10px 0px 30px 0px;

        .border-row {
            padding: 0px 13px 0px 0px;
            margin: 0px -16px 0px 0px;
            position: relative;
            z-index : 1;

            &:before {
              @extend .border-right;
                content: "";
                position: absolute;
                bottom: 112px;
                right: 0;
                height: 87%;
            }
        }

        .row-left {
          min-width: 265px;
          padding-right: 15px;

          .tab-winner {
            border-bottom-right-radius: 4px;
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
  }
</style>