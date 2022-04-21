<template>
  <div class="navbar-header">
    <div class="header-container">
      <div class="header">
        <NuxtLink to="/" class="header-logo">
            <amp-img alt="site logo" :src="image" width="300" height="41" layout="responsive" class="desktop"></amp-img>
        </NuxtLink>
        <div class="hidden-input">
          <LoginForm  :number="number" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
      components: {
          LoginForm: () => import('../LoginForm'),
      },
      data() {
        return {
          image: "/images/sk-image/SK-Logo-New.png",
          number: "1234",
        }
      },
  }
</script>

<style lang="scss" amp-boilerplate>
  .navbar-header {
     @extend .header-image-br-ig;

    .header-container {
       @extend .container-size;
       @extend .magrin-0-auto;

      .header {
        @extend .z-index-1;
        position: relative;
        height: 60px;
        width: 100%;
        
        .header-logo {
          @extend .display-inline-block;
          width: 150px;
          height: 100%;
          padding: 20px 0px 0px;
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
      }
    }
  }
</style>