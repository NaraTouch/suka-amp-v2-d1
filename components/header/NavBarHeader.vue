<template>
  <div class="navbar-header">
    <div class="header-container">
      <div class="header">
        <NuxtLink to="/" class="header-logo">
            <amp-img alt="site logo" src="/images/sk-image/SK-Logo-New.png" width="300" height="41" layout="responsive" class="desktop"></amp-img>
        </NuxtLink>
        <div class="hidden-input">
          <LoginForm />
        </div>
        <!-- <button class="header-nav-icon" on='tap:sidebar.toggle'>
            <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" fill="currentColor" class="bi bi-list" viewBox="0 0 16 16">
                <path fill-rule="evenodd" d="M2.5 12a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5z"/>
            </svg>
        </button> -->
        <!-- <amp-sidebar id="sidebar" layout="nodisplay" side="right">
            <div role="button" aria-label="close sidebar" on="tap:sidebar.toggle" tabindex="0" class="close-sidebar">✕</div>
            <ul class="sidebar">
                <li><a href="#">Example 1</a></li>
                <li><a href="#">Example 2</a></li>
                <li><a href="#">Example 3</a></li>
            </ul>
        </amp-sidebar> -->
      </div>
    </div>
  </div>
</template>

<script>
export default {
    components: {
         LoginForm: () => import('../LoginForm'),
    }
}
</script>

<style lang="scss" scoped>
  .navbar-header {
     @extend .header-image-br-ig;
    background-repeat: repeat-x;
    background-size: contain;

    .header-container {
       @extend .container-size;
       margin: 0 auto;

      .header {
        position: relative;
        height: 60px;
        width: 100%;
        z-index: 99999;
        
        .header-logo {
          width: 150px;
          height: 100%;
          // margin-left: 15px;
          display: inline-block;
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
        .header-clear {
          height: 50px;
        }
      }

      .container-div {
        margin: 0px 20px;
      }
    }
  }
</style>