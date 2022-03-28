<template>
  <!-- <section class="container"> -->
     <header class="header bg-gradient-1">
       <script async custom-element="amp-script" src="https://cdn.ampproject.org/v0/amp-script-0.1.js"></script>
      <NuxtLink to="/" class="header-logo">
        <amp-img
          alt="site logo"
          src="/images/logo-small.png"
          width="100"
          height="40"
          layout="responsive"
          class="desktop"
        >
        </amp-img>
        <amp-img
          alt="site logo"
          src="/images/logo-small-test.png"
          width="100"
          height="40"
          layout="responsive"
          class="mobile"
        >
        </amp-img>
      </NuxtLink>
      <div class="hidden-input">
        <DesktopForm />
       
      </div>
      <button class="header-nav-icon" on='tap:sidebar.toggle'>
        <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" fill="currentColor" class="bi bi-list" viewBox="0 0 16 16">
          <path fill-rule="evenodd" d="M2.5 12a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5z"/>
        </svg>
      </button>
      <div class="container-div">
        <Navigation />
        <RunningText />
        
     <p [text]="'Hello ' + foo">Hello World</p>

    <button on="tap:AMP.setState({foo: 'Interactivity'})">
      Say "Hello Interactivity"
    </button>
      </div>
    </header>
  <!-- </section> -->
</template>

<script>
export default {
  components: {
    DesktopForm: () => import('../components/DesktopForm'),
    Navigation: () => import('../components/Navigation'),
    RunningText: () => import('../components/RunningText'),
    CarouselGame: () => import('../components/CarouselGame'),
    CountAnimation: () => import('../components/CountAnimation'),
    LoadingNumber: () => import('../components/loadingNumber'),
  },
  methods: {
    say: function (message) {
      alert(message)
    }
  }
}
</script>

<style lang="scss" scoped>
p {
  color: red;
}
  .header {
    position: fixed;
    height: 50px;
    width: 100%;
    z-index: 99999;
    border-bottom: solid 1px rgba(0,0,0,0.1);
    .header-logo {
      width: 100px;
      height: 100%;
      margin-left: 15px;
      display: block;
    }
    .header-nav-icon {
      overflow: hidden;
      background-color: transparent;
      border: none;
      position: absolute;
      line-height: 65px;
      text-align: center; 
      width: 60px;
      display: block;
      font-size: 14px;
      right: 0px; 
      top: 3px;
      bottom: 0px;
      color: $text-color-1;
    }
    .header-clear {
      height: 50px;
    }
    .container-div {
      margin: 0px 20px;
    }
  }

  @media #{$sm-device} {
    .header {
      .hidden-input:first-of-type {
          visibility: hidden;
      }
      .hidden-input:last-of-type {
          visibility: hidden;
      }
      .header-logo[data-v-0957edea] {
          margin-inline: auto;
      }
      // desktop
      .desktop {
        display: none;
      }
    }
    .bg-gradient-1[data-v-0957edea] {
        background: $color-black;
        // background: #000000;
    }
  }
  @media #{$sm-down-device} {
    .header {
      .mobile {
        display: none;
      }
    }
  }
</style>
