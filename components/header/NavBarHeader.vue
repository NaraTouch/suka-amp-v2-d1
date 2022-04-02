<template>
    <div class="navbar-header">
        <div class="header bg-gradient-2">
            <NuxtLink to="/" class="header-logo">
                <amp-img alt="site logo" src="/images/logo-small.png" width="100" height="40" layout="responsive" class="desktop"></amp-img>
                <amp-img alt="site logo" src="/images/logo-small-test.png" width="100" height="40" layout="responsive" class="mobile"></amp-img>
            </NuxtLink>
            <div class="hidden-input">
              <LoginForm />
            </div>
            <button class="header-nav-icon" on='tap:sidebar.toggle'>
                <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" fill="currentColor" class="bi bi-list" viewBox="0 0 16 16">
                    <path fill-rule="evenodd" d="M2.5 12a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5z"/>
                </svg>
            </button>
            <amp-sidebar id="sidebar" layout="nodisplay" side="right">
                <div role="button" aria-label="close sidebar" on="tap:sidebar.toggle" tabindex="0" class="close-sidebar">✕</div>
                <ul class="sidebar">
                    <li><a href="#">Example 1</a></li>
                    <li><a href="#">Example 2</a></li>
                    <li><a href="#">Example 3</a></li>
                </ul>
            </amp-sidebar>
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
    padding: 0px 192px;
    border-bottom: solid 1px rgba(0,0,0,0.1);
    background-color: $color-gray;
    .header {
      position: relative;
      // position: fixed;
      height: 50px;
      width: 100%;
      z-index: 99999;
      
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
    }

    .container-div {
      margin: 0px 20px;
    }

    .bg-gradient-2[data-v-2a183b29] {
      // @extend .bg-gradient-1;
      background: $color-gray;
      // background: #ffa800;
      // background: linear-gradient(0deg, #ffa800, #ffcd02 35%, #ffcd02)
    }

    @media #{$sm-device} {
      .header {
        .hidden-input:first-of-type {
            visibility: hidden;
        }
        .hidden-input:last-of-type {
            visibility: hidden;
        }
        .header-logo {
          margin-left: auto;
          margin-right: auto;
        }
        // desktop
        .desktop {
          display: none;
        }
        
      }
      .bg-gradient-2[data-v-2a183b29] {
          background: $color-black;
      }
    }
    @media #{$sm-down-device} {
      .header {
        .mobile {
          display: none;
        }
      }
    }
  }
</style>