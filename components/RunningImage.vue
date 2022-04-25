<template>
    <div class="running-dev">
        <div class="running-text">
            <div class="display-row" v-for="(item, index) in items" :key="index">
                <div class="line"></div>
                <ImageIcon :customClassFirst="item.classFirst"  :customClassSecond="item.classSecond" />
            </div>
        </div>
    </div>
</template>

<script>
export default {
    components: {
        ImageIcon: () => import('./ImageIcon'),
    },
    data() {
        return {
            items: [
                { classFirst: "item-jackopt", classSecond: "item-idnlive" },
                { classFirst: "item-jackopt", classSecond: "item-pg" },
                { classFirst: "item-jackopt", classSecond: "item-idnlive" }
            ],
        }
    },
}
</script>

<style lang="scss" amp-boilerplate>
    .running-dev {
        @extend .running-image-br-ig;
        @extend .color-white;
        @extend .border-radius-3px;
        @extend .border-cr-white;
        padding: 8px;
        overflow: hidden;

        .running-text {
            @extend .display-flex;
            -moz-animation: marquee 15s linear infinite;
            -webkit-animation: marquee 15s linear infinite;
            animation: marquee 15s linear infinite;

            .display-row {
                @extend .display-flex;
        
                &:first-child {
                    .line {
                        width: 0px;
                        background: $color-white;
                        margin: 0px 10px;
                    }
                }
            
                .line {
                    width: 1px;
                    background: $color-white;
                    margin: 0px 10px;
                }
            }
        }

        @-moz-keyframes marquee {
            0% { transform: translateX(100%); }
            100% { transform: translateX(-100%); }
        }
        @-webkit-keyframes marquee {
            0% { transform: translateX(100%); }
            100% { transform: translateX(-100%); }
        }
        @keyframes marquee {
            0% {
                -moz-transform: translateX(100%);
                -webkit-transform: translateX(100%);
                transform: translateX(100%)
            }
            100% {
                -moz-transform: translateX(-100%);
                -webkit-transform: translateX(-100%);
                transform: translateX(-100%);
            }
        }
    }
</style>