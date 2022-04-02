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
            jackport: '../images/running-icon/jackpot.png',
            idn: '../images/running-icon/idn.png',
            pg: '../images/running-icon/idn.png',
            widthImage: '100px',
            heightImage: '20px',
            cardItems: [
                {
                    imageOne: '../images/running-icon/jackpot.png',
                    imageTwo: '../images/running-icon/idn.png',
                    widthImage: '100px',
                    heightImage: '20px',
                },
                {
                    imageOne: '../images/running-icon/jackpot.png',
                    imageTwo: '../images/running-icon/idn.png',
                    widthImage: '100px',
                    heightImage: '20px',
                },
                {
                    imageOne: '../images/running-icon/jackpot.png',
                    imageTwo: '../images/running-icon/idn.png',
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
        background-color: $color-black;
        color: $color-white;
        padding: 15px;
        border: 1px solid $color-white;
        border-radius: 5px;
        overflow: hidden;
        .running-text {
            -moz-animation: marquee 15s linear infinite;
            -webkit-animation: marquee 15s linear infinite;
            animation: marquee 15s linear infinite;
            display: flex;
            .row {
                display: flex;
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