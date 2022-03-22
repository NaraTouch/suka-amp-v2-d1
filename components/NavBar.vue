<template>
  <div>
    <header class="header bg-gradient-1">
      <NuxtLink to="/" class="header-logo">
        <amp-img
          alt="site logo"
          src="/images/logo-small.png"
          width="100"
          height="40"
          layout="responsive"
        >
        </amp-img>
      </NuxtLink>
      <DesktopForm />
      <button class="header-nav-icon" on='tap:sidebar.toggle'>
        <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" fill="currentColor" class="bi bi-list" viewBox="0 0 16 16">
          <path fill-rule="evenodd" d="M2.5 12a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5z"/>
        </svg>
      </button>
    </header>
    <div class="header-clear"></div>
  </div>
</template>
<script>
import DesktopForm from "~/components/DesktopForm.vue";

export default {
  components: {
    DesktopForm,
  },
};
</script>
<style lang="scss" scoped>
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
    top: 0px;
    bottom: 0px;
    color: $text-color-1;
  }
  .header-clear {
    height: 50px;
  }
}
</style>
