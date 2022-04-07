<template>
    <div class="stay-connected-list">
        <div class="header">
            <span>Stay connected</span>
        </div>
        <div class="inner-grid-connected">
            <amp-list class="connected" width="auto" height="70" layout="fixed-height" src="/data/connection-list.json" v-html="imageList" />
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            imageList: `
                <template type="amp-mustache">
                    <amp-carousel  class="connected-image" id="custom-button"  width="40" height="40" type="slides" >
                        <a href="{{url}}" target="_blank"> <amp-img src="{{logo}}" width="40" height="40" layout="responsive" alt="AMP Carousel"></amp-img></a>
                    </amp-carousel>
                </template>
            `
        }
    },
}
</script>

<style lang="scss">
    .stay-connected-list {
        // margin: 15px 0px 0px 0px;
        .header {
            text-align: justify;
            margin: 10px 0px 10px 20px;
            span {
                font-size: 16px;
                font-weight: 400;
            }
        }
        .inner-grid-connected {
            margin: 10px 0px 0px 10px;
            .connected {
                    margin: 0px 0px -8px 7px;
                .connected-image {
                    margin: 0px 10px;
                    &:first-child {
                        margin: 0px 8px 0px 0px;
                    }
                    &:last-child {
                        margin: 0px 0px 0px 0px;
                    }
                }
            }
        }
    }
</style>