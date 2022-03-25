<template>
    <div>
        <div class="running-dev">
            <div class="running-text">
                <div class="row">
                    <div>
                        <hr />
                    </div>
                    <ImageIcon :src="jackport"  :width="widthImage" :height="heightImage" />
                   <LoadingComponent />
                    <ImageIcon :src="idn"  :width="widthImage" :height="heightImage" />
                </div>
                <div class="row">
                    <div>
                        <hr />
                    </div>
                    <ImageIcon :src="jackport"  :width="widthImage" :height="heightImage" />
                   <LoadingComponent />
                    <ImageIcon :src="idn"  :width="widthImage" :height="heightImage" />
                </div>
                <div class="row">
                    <div>
                        <hr />
                    </div>
                   <ImageIcon :src="jackport"  :width="widthImage" :height="heightImage" />
                   <LoadingComponent />
                   <ImageIcon :src="pg"  :width="widthImage" :height="heightImage" />
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    components: {
        LoadingComponent: () => import('./loadingNumber'),
        ImageIcon: () => import('./ImageIcon'),
    },
    data() {
        return {
            jackport: '../images/running-icon/jackpot.png',
            idn: '../images/running-icon/idn.png',
            pg: '../images/running-icon/idn.png',
            widthImage: '100px',
            heightImage: '20px'
        }
    },
}
</script>

<style lang="scss" scoped>
    .running-dev {
        background-color: $color-black;
        color: $color-white;
        padding: 10px;
        border: 1px solid $border-color-1;
        border-radius: 15px;
        overflow: hidden;
        .running-text {
            -moz-animation: marquee 15s linear infinite;
            -webkit-animation: marquee 15s linear infinite;
            animation: marquee 15s linear infinite;
            display: flex;
            .row {
                display: flex;
            }
            hr {
                height: 100%;
                margin: 0px 10px;
                border: 1px solid $border-color-1;
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