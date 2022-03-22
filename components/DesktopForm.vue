<template>
  <div>
    <form class="d-login-form" method="post" action-xhr="/documentation/examples/api/submit-form-input-text-xhr" target="_top">
      <div>
        <div class="left-inner-addon">
            <span class="form-control-feedback bg-gradient-1">
              <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-person-fill" viewBox="0 0 16 16">
                <path d="M3 14s-1 0-1-1 1-4 6-4 6 3 6 4-1 1-1 1H3zm5-6a3 3 0 1 0 0-6 3 3 0 0 0 0 6z"/>
              </svg>
            </span>
            <input type="password"
                   class="form-control" 
                   placeholder="Left icon" />
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
    line-height: 45px;
    text-align: center; 
    display: block;
    font-size: 14px;
    right: 60px; 
    top: 0px;
    bottom: 0px;
  .left-inner-addon {
      position: relative;
      padding-bottom: 1em;
  }
  .left-inner-addon span {
    position: absolute;
    padding: 12px 12px;
    pointer-events: none;
}
}
</style>
