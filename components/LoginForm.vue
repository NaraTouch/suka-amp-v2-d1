<template>
  <div>
    <form class="d-login-form" method="post" action-xhr="/documentation/examples/api/submit-form-input-text-xhr" target="_top">
      <div class="left-inner-addon">
        <div class="mr-password" >
          <a href="#"><span>Lupa password?</span></a>
        </div>

        <div class="input-mr">
          <span class="span-style">
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-person-fill" viewBox="0 0 16 16">
            <path d="M3 14s-1 0-1-1 1-4 6-4 6 3 6 4-1 1-1 1H3zm5-6a3 3 0 1 0 0-6 3 3 0 0 0 0 6z"/>
            </svg>
          </span>
          <input type="password" class="input-custom-style" placeholder="username" />
        </div>

        <div class="input-mr">
          <span class="span-style">
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-person-fill" viewBox="0 0 16 16">
            <path d="M3 14s-1 0-1-1 1-4 6-4 6 3 6 4-1 1-1 1H3zm5-6a3 3 0 1 0 0-6 3 3 0 0 0 0 6z"/>
            </svg>
          </span>
          <input type="password" class="input-custom-style" placeholder="password" />
        </div>

        <div class="input-mr">
           <span class="span-style span-style-code">{{ number }}</span>
          <input type="password" class="input-custom-style-code" placeholder="code" />
        </div>

        <div>
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
        margin: 5px;
      }

      .input-mr {
          margin-right: 5px;
      }

      .span-style {
        position: absolute;
        padding: 6px 0px 0px 5px;
      }

      .span-style-code {
        @extend .span-style;
        @extend .btn-color-Masuk;
        padding: 6px 5px 7px 5px;
        border-top-left-radius: 2px;
        border-bottom-left-radius: 2px;
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
      }

      .btn-color-Masuk {
        @extend .btn-bg-red;
        @extend .color-white;
      }

      .btn-color-Daftar {
        @extend .btn-bg-white;
      }

      svg { 
        fill: $color-gray; 
      }

      input:focus {
        outline: none;
      }
    }
  }
</style>