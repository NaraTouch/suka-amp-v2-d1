<template>
  <div>
    <form class="d-login-form" method="post" action-xhr="/documentation/examples/api/submit-form-input-text-xhr" target="_top">
      <div class="left-inner-addon">
        <div class="mr-password" >
          <a href="#"><span>Lupa password?</span></a>
        </div>

        <div class="input-mr">
          <div class="input-icon"><div class="bg-position-usename"></div></div>
          <input type="password" class="input-custom-style" placeholder="username" />
        </div>

        <div class="input-mr">
          <div class="input-icon"><div class="bg-position-password"></div></div>
          <input type="password" class="input-custom-style" placeholder="password" />
        </div>

        <div class="input-mr">
           <span class="span-style span-style-code">{{ number }}</span>
          <input type="password" class="input-custom-style-code" placeholder="code" />
        </div>

        <div class="btn-style" >
          <button class="btn btn-color-Masuk">Masuk</button>
          <button class="btn btn-color-Daftar">Daftar</button>
        </div>
      </div>
    </form>
  </div>
</template>

<script>
  export default {
    props: {
      number: String,
    }
  };
</script>

<style lang="scss" amp-boilerplate>
  .d-login-form {
    overflow: hidden;
    background-color: transparent;
    border: none;
    position: absolute;
    text-align: center; 
    display: block;
    font-size: 14px;
    right: 0px; 
    top: 15px;
    bottom: 0px;

    .left-inner-addon {
      position: relative;      
      display: flex;

      .mr-password {
        margin: 5px 5px 0px 0px;
      }

      .input-mr {
        display: flex;
        position: relative;
        margin: 0px 0px 0px 7px;

        .input-icon {
          margin: 7px -20px 0px 0px;
          z-index: 1;

          div {
            background: url(/images/input-icon/input-icon.png) no-repeat;
            height: 16px;
            width: 16px;
          }

          .bg-position-usename {
            background-position: 0px 0px;
          }
          
          .bg-position-password {
            background-position: -18px 0px;
          }
        }
      }

      .btn-style {
        margin-left: 5px;
      }

      .span-style {
        position: absolute;
        padding: 6px 0px 0px 5px;
      }

      .span-style-code {
        @extend .span-style;
        @extend .btn-color-Masuk;
        padding: 7px 5px 8px 5px;
        border-top-left-radius: 2px;
        border-bottom-left-radius: 2px;
        margin: 0px 0px 0px -3px;
      }

      a {
        text-decoration: none;
        @extend .color-white;
        
        span {
          font-size: 13px;
        }
      }

      .input-custom-style {
        @extend .border-radius-3px;
        padding: 6px 2px 6px 25px;
        border: 1px solid $color-gray;
        width: 150px;
      }

      .input-custom-style-code {
         @extend .input-custom-style;
         padding: 6px 2px 6px 45px;
      }

      .btn {
        @extend .border-radius-3px;
        @extend .btn-font;
        padding: 7px 15px 7px 13px;
        cursor: pointer;
      }

      .btn-color-Masuk {
        @extend .btn-bg-red;
        @extend .color-white;
      }

      .btn-color-Daftar {
        @extend .btn-bg-white;
      }
     
      input:focus {
        outline: none;
      }
    }
  }
</style>