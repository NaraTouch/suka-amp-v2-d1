<template>
    <div class="running-dev">
        <div class="running-text">
            <div class="row" v-for="(cardItem, index) in cardItems" :key="index">
               <div class="line"></div>
                <ImageIcon :src="cardItem.imageOne"  :width="cardItem.widthImage" :height="cardItem.heightImage" />

                <LoadingComponent />

                <ImageIcon :src="cardItem.imageTwo"  :width="cardItem.widthImage" :height="cardItem.heightImage" />
            </div>
        </div>
    </div>
</template>

<script>
export default {
    components: {
        LoadingComponent: () => import('./loadingNumber'),
        ImageIcon: () => import('./ImageIcon'),
        CountAnimation: () => import('./CountAnimation'),
    },
    data() {
        return {
            jackport: '../images/running-ig/jackpot.png',
            idn: '../images/running-ig/idn.png',
            pg: '../images/running-ig/idn.png',
            widthImage: '100px',
            heightImage: '20px',
            cardItems: [
                {
                    imageOne: '../images/running-ig/jackpot.png',
                    imageTwo: '../images/running-ig/idn.png',
                    widthImage: '100px',
                    heightImage: '20px',
                },
                {
                    imageOne: '../images/running-ig/jackpot.png',
                    imageTwo: '../images/running-ig/idn.png',
                    widthImage: '100px',
                    heightImage: '20px',
                },
                {
                    imageOne: '../images/running-ig/jackpot.png',
                    imageTwo: '../images/running-ig/idn.png',
                    widthImage: '100px',
                    heightImage: '20px',
                }
            ]
        }
    },
}
</script>

<style lang="scss" scoped>
    .running-dev {
        @extend .running-image-br-ig;
        @extend .color-white;
        @extend .border-radius-3px;
        padding: 15px;
        border: 1px solid $color-white;
        overflow: hidden;

        .running-text {
            @extend .display-flex;
            -moz-animation: marquee 15s linear infinite;
            -webkit-animation: marquee 15s linear infinite;
            animation: marquee 15s linear infinite;

            .row {
                @extend .display-flex;
                
                 &:first-child {
                        .line {
                        width: 0px;
                        background: $border-color-1;
                        margin: 0px 10px;
                    }
                }
                
                .line {
                    width: 1px;
                    background: $border-color-1;
                    margin: 0px 10px;
                }
            }
        }
        @-moz-keyframes marquee {
            0% {
                transform: translateX(100%);
            }
            100% {
                transform: translateX(-100%);
            }
        }
        @-webkit-keyframes marquee {
            0% {
                transform: translateX(100%);
            }
            100% {
                transform: translateX(-100%);
            }
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