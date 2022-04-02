<template>
    <div class="stay-connected-list">
        <div class="header">
            <span>Stay connected</span>
        </div>
        <div>
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
                    <amp-carousel  class="connected-image" id="custom-button"  width="50" height="50" type="slides" >
                        <a href="{{url}}" target="_blank"> <amp-img src="{{logo}}" width="50" height="50" layout="responsive" alt="AMP Carousel"></amp-img></a>
                    </amp-carousel>
                </template>
            `
        }
    },
}
</script>

<style lang="scss">
    .stay-connected-list {
        margin: 15px 0px 0px 0px;
        .header {
            text-align: justify;
            margin: 10px 0px 10px 20px;
            span {
                font-size: 16px;
                font-weight: 400;
            }
        }
        .list-overflow[overflow] {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            }
            .connected {
                margin: 10px 0px 0px 0px;
                .connected-image {
                    margin: 0px 15px;
                }
            }
    }
</style>