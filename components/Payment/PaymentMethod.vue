<template>
    <div class="payment-methods">
        <div class="header">
            <span>Payment Method</span>
        </div>
        <div class="grid-container-item">
            <div class="test1">
                <amp-list class="connected" width="auto" height="200" layout="fixed-height" src="/data/bank-list-one.json" v-html="banlList" />
            </div>
             <div class="test2">
                <amp-list class="connected" width="auto" height="200" layout="fixed-height" src="/data/bank-list-one.json" v-html="banlList" />
            </div>
        </div>
        <div class="button-style">
            <amp-img class="image-size" on="tap:lightbox1" role="button" tabindex="0" :src="imagePromosi" width="220" height="30"   />
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
            padding: 10px 0px 10px 15px;
            color: $color-white;
            span {
                font-size: 16px;
                font-weight: 400;
            }
        }
        .grid-container-item {
                display: grid;
                grid-template-columns: 1fr 1fr;
                // grid-gap: 5px;
            .mr-r-l {
                padding: 0px 10px 10px 10px;   
            }
            // .amp-padding-image {
            //     margin: 0px 5px;
            // }
        }
        .button-style { 
            text-align: center;

            button {
                display: inline-block;
                max-width: 100%;
                width: auto;
                height: auto;
                line-height: 1.3em;
                padding: 0.5em 1em;
                margin-right: 0.3em;
                
                font-family: 'Poppins', sans-serif;
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
                &:hover {
                    // transform: translateY(-.125em);
                    color: $color-white;
                    background-color: $btn-color-1;
                }
            }
        }
    }
</style>