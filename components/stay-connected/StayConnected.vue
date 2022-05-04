<template>
  <div class="stay-connected-list">
    <div class="title-stay-connection">
      <span>Stay connected</span>
    </div>

    <div class="body-connected">
      <ul class="menus">
        <li class="item-ig"><a class="link" href="#"><div></div></a></li>
        <li class="item-fb"><a class="link" href="#"><div></div></a></li>
        <li class="item-brid"><a class="link" href="#"><div></div></a></li>
        <li class="item-youtube"><a class="link" href="#"><div></div></a></li>
      </ul>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        
      };
    },
  };
</script>

<style lang="scss" amp-boilerplate>
  .stay-connected-list { 
    .title-stay-connection {
      padding: 20px 0px 0px 15px;
      @extend .color-white;
    }

    .body-connected {
      padding: 10px 10px 20px 10px;

      .menus {
        @extend .display-grid;
        list-style-type: none;
        padding: 0px;
        grid-template-columns: 1fr 1fr 1fr 1fr;
        
        li {
          font-size: 16px;
          font-family: "Trebuchet MS", Arial, sans-serif;

          a {
            div {
              background: url(/images/brand-logo/stay-connected.png) no-repeat;
              height: 50px;
              width: 50px;
            }
          }
        }

        .item-ig { a { div { background-position: 0px 0px; } } }

        .item-fb { a { div { background-position: -50px 0px; } } }

        .item-brid { a { div { background-position: 0px -50px; } } }
        
        .item-youtube { a { div { background-position: -50px -50px; } } }
      }
    }
  }
</style>
