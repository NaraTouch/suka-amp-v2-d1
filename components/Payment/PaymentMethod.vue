<template>
    <div class="payment-methods">
        <div class="header">
            <span class="span-left"></span>
            <span class="span-right">Payment Method</span>
        </div>
        <div class="grid-container-item">
            <div>
                <amp-list class="connected" width="auto" height="200" layout="fixed-height" src="/data/bank-list-one.json" v-html="banlList" />
            </div>
             <div >
                <amp-list class="connected" width="auto" height="200" layout="fixed-height" src="/data/bank-list-two.json" v-html="banlList" />
            </div>
        </div>
        <div class="button-style">
            <button class="btn btn-color-promosi">Lihat semua</button>
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
       }
   },
}
</script>
<style lang="scss">
    .payment-methods {
        .header {
            text-align: justify;
            padding: 20px 0px 15px 15px;
            color: $color-white;

            .span-left {
                background-image: url(/images/bank/sidebar-payment-logos.png);
                background-repeat: no-repeat;
                width: 40px;
                height: 21px;
                display: block;
                float: left;
                margin: -3px 10px 0px 0px;
                border-radius: 2px;
            }

            .span-right {
                font-size: 15px;
                font-weight: 500;
            }
        }
        .grid-container-item {
            display: grid;
            grid-template-columns: 1fr 1fr;
            grid-gap: 10px;
            margin: 0px 15px;

            .mr-r-l {
                padding: 0px 0px 10px 0px;
            }
        }
        .button-style { 
            text-align: center;
            margin: 5px 0px 5px 0px;

            .btn {
                border: 1px;
                padding: 8px 40px 8px 40px;
                border-radius: 3px;
                font-weight: 600;
            }
            
            .btn-color-promosi {
                @extend .btn-bg-red;
                color: $color-white;
            }
        }
    }
</style>