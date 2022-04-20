<template>
  <div>
    <form class="d-login-form" method="post" action-xhr="/documentation/examples/api/submit-form-input-text-xhr" target="_top">
      <div>
        <div class="left-inner-addon">
          <span><a href="">Lupa password?</a></span>
          <span class="form-control-feedback span-style">
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-person-fill" viewBox="0 0 16 16">
            <path d="M3 14s-1 0-1-1 1-4 6-4 6 3 6 4-1 1-1 1H3zm5-6a3 3 0 1 0 0-6 3 3 0 0 0 0 6z"/>
            </svg>
          </span>
          <input type="password" class="form-control input-custom-style" placeholder="input text" />

          <span class="form-control-feedback span-style">
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-person-fill" viewBox="0 0 16 16">
            <path d="M3 14s-1 0-1-1 1-4 6-4 6 3 6 4-1 1-1 1H3zm5-6a3 3 0 1 0 0-6 3 3 0 0 0 0 6z"/>
            </svg>
          </span>
          <input type="password" class="form-control input-custom-style" placeholder="input text" />

          <input type="password" class="form-control input-custom-style" placeholder="input text" />

          <button class="btn btn-color-Masuk">Masuk</button>
          <button class="btn btn-color-Daftar">Daftar</button>
        </div>
      </div>
    </form>
  </div>
</template>

<script>
  export default {
 
  };
</script>

<style lang="scss" >
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

      .span-style {
        position: absolute;
        padding: 6px 0px 0px 5px;
      }

      a {
        text-decoration: none;
        @extend .color-white;
      }

      .input-custom-style {
        @extend .border-radius-3px;
        padding: 6px 2px 6px 25px;
        border: 1px solid $color-gray;
        width: 150px;
      }

      .btn {
        @extend .border-radius-3px;
        padding: 6px 15px 6px 13px;
        @extend .btn-font;
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