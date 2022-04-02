<template>
  <div>
    <form class="d-login-form" method="post" action-xhr="/documentation/examples/api/submit-form-input-text-xhr" target="_top">
      <div>
        <div class="left-inner-addon">
            <span class="span-text">Lupa Password ?</span>
            <span class="form-control-feedback span-style">
              <svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" fill="currentColor" class="bi bi-person-fill" viewBox="0 0 16 16">
                <path d="M3 14s-1 0-1-1 1-4 6-4 6 3 6 4-1 1-1 1H3zm5-6a3 3 0 1 0 0-6 3 3 0 0 0 0 6z"/>
              </svg>
            </span>
            <input type="password" class="form-control input-custom-style" placeholder="input text" />

             <span class="form-control-feedback span-style">
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
  top: 12px;
  bottom: 0px;
  .left-inner-addon {
    position: relative;
    .span-text {
      color: $color-white;
      margin-right: 10px;
    }
    .span-style {
      position: absolute;
      padding: 4px 6px;
      margin: 1px -14px 0px -1px;
      border-radius: 4px;
      background-color: $rgb-light-1;
    }
    .input-custom-style {
      // @extend .input-gradient;
          padding: 6px 12px 6px 30px;
      border: 1px solid black;
      border-radius: 4px;
      box-shadow: var(--box-shadow-1);
      // border-radius: 15px;
    }
    button { 
      display: inline-block;
      max-width: 100%;
      width: auto;
      height: auto;
      line-height: 1.3em;
      padding: 0.8em 7em;
      margin-right: 0.3em;
      
      font-size: 1em;
      font-weight: 700;
      
      color: #005af0;
      text-decoration: none;
      text-align: center;
      
      border: 0;
      border-radius: 3px;
      background-color: #fff;
      
      box-shadow: var(--box-shadow-1);
      transition: 
          transform .3s cubic-bezier(.25,.1,.25,1),
          box-shadow .3s cubic-bezier(.25,.1,.25,1);
      
      cursor: pointer;
    }
    .btn {
      // border-radius: 13px;
      // border: 1px solid #ffa800;
      padding: 3px 15px 5px 15px;
    }
    .btn-color {
      background: $btn-color-1;
      color: $color-white;
    }
    svg{ 
      fill:  $color-white; 
    }
    input:focus {
      outline: none;
    }
  }
  
}
</style>
