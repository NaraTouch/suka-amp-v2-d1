<template>
  <section >
    <div class="grid-body">
      <header class="page-header">
        <NavBarHeader />
      </header>

      <div class="container">
        <!-- running-text -->
        <div class="running-text">
          <running-text />
        </div>

        <!-- navbar -->
        <nav class="navbar">
            <nav-image />
        </nav>

        <!-- running-image -->
        <div class="running-image">
          <running-image />
        </div>

        <!-- left -->
        <aside class="tab-winner">
          <TabWinner />
        </aside>

        <div class="ads-image">
          <Slider :slide-list="sliderPromotion" :slider="slderCondition" />
        </div>

        <div class="stay-connected">
          <h2>stay connected</h2>
          <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Libero tempore adipisci rem illo esse distinctio tempora ducimus. Porro, molestias sequi placeat rerum reprehenderit illo eum laudantium culpa unde, sunt eligendi.</p>
        </div>

        <div class="payment-method">
          <h2>Payment Methods</h2>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolores repellat accusamus corrupti eligendi sunt corporis, fuga quas velit vitae, ex dolorum saepe. Perferendis inventore dicta placeat similique doloribus obcaecati voluptates.</p>
        </div>
        <div class="content-text">
          <h2>content-text</h2>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Alias reiciendis doloremque quidem cupiditate exercitationem! Optio ex quasi perspiciatis suscipit corrupti, aut nisi est error quod provident tempora commodi, velit consequatur?</p>
        </div>

        <!-- right -->
        <div class="slider-image">
          <Slider :slide-list="sliderImage" />
          <SliderPath />
        </div>

        <!-- <div class="button-slider">
          <h2>button button button</h2>
        </div> -->

        <div class="card">
          <h2>card</h2>
          <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Corporis soluta vitae necessitatibus officia, nemo, dolore natus neque perspiciatis amet ut iusto voluptates ad libero sapiente! Quibusdam optio perspiciatis blanditiis ut.</p>
        </div>

        <!-- footer -->
        <footer class="footer">
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Cum inventore eveniet beatae rem provident atque ducimus! Adipisci culpa, dolor dolorum cupiditate sit sunt eos, ad hic est ipsum provident nemo!</p>
        </footer>
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
    SliderPath: () => import('../components/slider/SliderPath'),
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
      // display: grid;
      // grid-template-areas: 
      //   "running-text running-text"
      //   "navbar navbar"
      //   "running-image running-image"
      //   "aside section"
      //   "footer footer";
      // grid-template-rows: 50px 100px 50px 1fr 50px;
      // grid-template-columns: 30% 1fr;
      // grid-row-gap: 10px;
      // grid-column-gap: 10px;
      // height: 100vh;
      // margin: 0;

      .content-text,.card,.button-slider,.payment-method,.ads-image,.stay-connected,.connected,.section, .aside,  .footer {
        // padding: 1.2em;
        background: gold;
      }

      .page-header {
        grid-area: page-header;
      }
      
      .running-text {
        grid-area: running-text;
      }

      .navbar {
        grid-area: navbar;
      }

      .running-image {
        grid-area: running-image;
      }
      // left
      .tab-winner {
        grid-area: tab-winner;
      }
      .stay-connected {
        grid-area: stay-connected;
      }
      .ads-image {
        grid-area: ads-image;
      }
      .payment-method {
        grid-area: payment-method;
      }
      .content-text {
        grid-area: content-text;
      }

      // right
      .card {
        grid-area: card;
      }
      .slider-image {
        grid-area: slider-image;
        background-image: url('/images/header/header-background.jpg');
      }
      .button-slider {
        grid-area: button-slider;
      }

      .footer {
        grid-area: footer;
      }

      @media #{$lg-down-device} {
            display: grid;
            grid-template-areas: 
              "running-text   running-text"
              "navbar         navbar"
              "running-image  running-image"
              "tab-winner     slider-image"
              "tab-winner     slider-image"
              "ads-image      card"
              "stay-connected card"
              "payment-method card"
              "content-text   card"
              "footer         footer";
            grid-template-rows: 50px 100px 50px 330px 50px 200px 100px 150px 100px 2fr 50px;
            // grid-template-rows: running-text navbar running-image tabwinner button ads-image stay-connect payment-methods content-text card footer;
            grid-template-columns: 30% 1fr;
            grid-row-gap: 10px;
            grid-column-gap: 10px;

            //tabwinner
            .aside {

            }
            // card
            .slider-image {

            }
            .section {}
        }

      // Mobile Landscpe
      // @media #{$md-device} { 

      // }

      // Mobile Landscpe
      @media #{$sm-down-device} { 
        // .grid-body {
        //   .container {
        //     display: grid;
        //     grid-template-areas: 
        //       "running-text running-text running-text"
        //       "navbar navbar"
        //       "running-image running-image"
        //       "aside section"
        //       "footer footer";
        //     grid-template-rows: 50px 100px 50px 1fr 50px;
        //     grid-template-columns: 30% 1fr;
        //     grid-row-gap: 10px;
        //     grid-column-gap: 10px;
        //     height: 100vh;
        //     margin: 0;
        //   }
        // }
      }
      @media #{$xs-device} { 

      }
    }
  }
</style>