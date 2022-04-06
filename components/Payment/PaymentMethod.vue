<template>
    <div class="payment-methods">
        <div class="header">
            <span>Payment Method</span>
        </div>

        <div class="grid-container-item">
            <div>
                <amp-list class="connected" width="auto" height="50" layout="fixed-height" src="/data/bank-list.json" v-html="banlList" />
            </div>
        </div>
        <div class="button-style">
            <button>Lihat semuna</button>
        </div>
    </div>
</template>

<script>
export default {
   data() {
       return {
           banlList: `
                 <template type="amp-mustache">
                    <amp-carousel  class="amp-padding-image" id="custom-button"  width="150" height="50" type="slides" >
                        <a href="{{link}}" target="_blank"> <amp-img src="{{image}}" width="200" height="50" layout="responsive" alt="AMP Carousel"></amp-img></a>
                    </amp-carousel>
                </template>
           `
       }
   },
}
</script>

<style lang="scss">
    .payment-methods {
        .header {
            text-align: justify;
            margin: 10px 0px 10px 20px;
            span {
                font-size: 16px;
                font-weight: 400;
            }
        }
        .grid-container-item {
            .amp-padding-image {
                margin: 0px 5px;
            }
        }
        .button-style { 
            margin-bottom: 15px;
            button {
            display: inline-block;
            max-width: 100%;
            width: auto;
            height: auto;
            line-height: 1.3em;
            padding: 0.8em 7em;
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