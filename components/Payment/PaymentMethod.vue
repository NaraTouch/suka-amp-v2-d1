<template>
    <div class="payment-methods">
        <div class="title-payment-methods">
            <title-image :customComponent="condition" :title="title" :image-title="titleIcon" :width="width" :height="height" :custom-class="custom" />
        </div>

        <div class="body-payment-methods">
            <ul class="menus">
                <li class="item-bank-bri"><a class="link" href="#"><div></div></a></li>
                <li class="item-bank-cimb"><a class="link" href="#"><div></div></a></li>
                <li class="item-bank-mandiri"><a class="link" href="#"><div></div></a></li>
                <li class="item-bank-damamon"><a class="link" href="#"><div></div></a></li>
                <li class="item-bank-bca"><a class="link" href="#"><div></div></a></li>
                <li class="item-bank-bni"><a class="link" href="#"><div></div></a></li>
                <li class="item-bank-permatal"><a class="link" href="#"><div></div></a></li>
                <li class="item-bank-panin"><a class="link" href="#"><div></div></a></li>
            </ul>
        </div>

        <div class="button-style">
            <button class="btn-color-promosi">Lihat semua</button>
        </div>
    </div>
</template>
<script>
export default {
   data() {
       return {
           banlList: `
                 <template type="amp-mustache">
                    <div class="mr-r-l">
                        <a href="{{link}}" target="_blank"> <amp-img src="{{image}}" width="200" height="80" layout="responsive" alt="AMP Carousel"></amp-img></a>
                    </div>
                </template>
           `,
           imagePromosi: "/images/button/Banner_Button_promosi_red.png",
           titleIcon: "images/bank/payment-method-icon.png",
           width: "40px",
           height: "23px",
           title: "Payment Method",
           custom: "custom",
           condition: false,
       }
   },
}
</script>
<style lang="scss" amp-boilerplate>
    .payment-methods {
        .title-payment-methods {    
            padding: 20px 0px 5px 14px;
        }

        .body-payment-methods {
            padding: 5px 13px 15px 13px;

            .menus {
                display: grid;
                grid-template-columns: 1fr 1fr;
                grid-gap: 10px;
                list-style-type: none;
                padding: 0px;

                li {
                    a {
                        div {
                            background: url(/images/bank/bank-image.png) no-repeat;
                            height: 47px;
                            width: 107px;
                            background-color: white;
                        }
                    }
                }
                .item-bank-bri { a { div { background-position: -3px 0px; } } }
                .item-bank-cimb { a { div { background-position: -113px 0px; } } }
                .item-bank-mandiri { a { div { background-position: -1px -55px; } } }
                .item-bank-damamon { a { div { background-position: -113px -55px; } } }
                .item-bank-bca { a { div { background-position: -4px -104px; } } }
                .item-bank-bni { a { div { background-position: -113px -104px; } } }
                .item-bank-permatal { a { div { background-position: -3px -160px; } } }
                .item-bank-panin { a { div { background-position: -113px -155px; } } }
            }
        }
        .button-style {
            margin: 0 auto;
            position: relative;
            display: table;
            
            .btn-color-promosi {
                @extend .btn-custom;
                @extend .btn-bg-red;
                @extend .color-white;
            }
        }
    }
</style>