<template>
  <div>
    <form class="d-login-form" method="post" action-xhr="/documentation/examples/api/submit-form-input-text-xhr" target="_top">
      <div>
        <div class="left-inner-addon">
            <span class="form-control-feedback bg-gradient-1 span-style">
              <svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" fill="currentColor" class="bi bi-person-fill" viewBox="0 0 16 16">
                <path d="M3 14s-1 0-1-1 1-4 6-4 6 3 6 4-1 1-1 1H3zm5-6a3 3 0 1 0 0-6 3 3 0 0 0 0 6z"/>
              </svg>
            </span>
            <input type="password" class="form-control input-custom-style" placeholder="input text" />

             <span class="form-control-feedback bg-gradient-1 span-style">
              <svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" fill="currentColor" class="bi bi-person-fill" viewBox="0 0 16 16">
                <path d="M3 14s-1 0-1-1 1-4 6-4 6 3 6 4-1 1-1 1H3zm5-6a3 3 0 1 0 0-6 3 3 0 0 0 0 6z"/>
              </svg>
            </span>
            <input type="password" class="form-control input-custom-style" placeholder="input text" />

            <button class="btn btn-color">Masuk</button>
            <button class="btn ">Masuk</button>
        </div>
    </div>
    </form>
  </div>
</template>
<script>
export default {
 
};
</script>

<style lang="scss" scoped>
.d-login-form {
  overflow: hidden;
  background-color: transparent;
  border: none;
  position: absolute;
  text-align: center; 
  display: block;
  font-size: 14px;
  right: 60px; 
  top: 13px;
  bottom: 0px;
  .left-inner-addon {
    position: relative;
    .span-style {
       position: absolute;
      padding: 0px 3px ;
      margin: 0px -25px 0px 0px;
      border-radius: 10px;
      background-color: $rgb-light-1;
    }
    .input-custom-style {
      @extend .input-gradient;
      padding: 2px 13px 1px 22px;
      border: 1px solid $rgb-light-1;
      border-radius: 14px;
    }
    .btn {
      border-radius: 10px;
      border: 1px solid $rgb-light-1;
    }
    .btn-color {
      background: $btn-color-1;
      color: $color-white;
    }
    svg{ 
      fill:  $color-white; 
    }
  }
  
}
</style>
