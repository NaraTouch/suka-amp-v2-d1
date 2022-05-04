<template>
    <div class="navbar-images">
        <ul class="menus">
            <li class="item-hot-game"><a class="link hot-game" href="/hotGame"><div><span>HOT GAME</span></div></a></li>
            <li class="item-slots"><a class="link" href="/slots"><div><span>Slots</span></div></a></li>
            <li class="item-sports"><a class="link" href="/sports"><div><span>Sports</span></div></a></li>
            <li class="item-casino"><a class="link" href="/casino"><div><span>Casino</span></div></a></li>
            <li class="item-poker"><a class="link" href="/poker"><div><span>Poker</span></div></a></li>
            <li class="item-arcade"><a class="link" href="/arcade"><div><span>Arcade</span></div></a></li>
            <li class="item-togel"><a class="link" href="/togel"><div><span>Togel</span></div></a></li>
            <li class="item-cock-fighter"><a class="link" href="/cockFighting"><div><span class="span-custom" >Cock Fighter</span></div></a></li>
            <li class="item-lucky-spain"><a on="tap:modalboxs" role="button" tabindex="0" class="link-padding"  ><div class="lucky-spain-image"></div></a></li>
        </ul>

        <!-- <div class="popup-style">
            <amp-lightbox class="z-index-style" id="modalboxs" layout="nodisplay">
                <div class="modalboxs">
                    <lucky-spin />
                </div>
            </amp-lightbox>
        </div> -->
    </div>
</template>

<script>
    export default {
        components: { 
            // LuckySpin: () => import('../popup/luckySpin'),
        },
    }
</script>

<style lang="scss" amp-boilerplate>
    .navbar-images {

        .popup-style {
            .z-index-style {
                z-index: 99999;
                .modalboxs {
                    background: rgba(0, 0, 0, 0.5);
                    width: 100%;
                    height: 100%;
                }

                .modal_boxs {
                    border-radius: 4px;
                    box-shadow: 0 9px 46px 8px rgb(0 0 0 / 14%), 0 11px 15px -7px rgb(0 0 0 / 12%), 0 24px 38px 3px rgb(0 0 0 / 20%);
                    position: absolute;
                    top: 3%;
                    transition: all 0.3s ease-in-out;
                    left: 0;
                    right: 0;
                    background-size: 40px 40px;
                    border-radius: 10px;
                    margin: 0 auto;
                }
            }
        }

        // custom border
        .border-style {
            border: 1px solid $color-white;
        }
        
        .menus {
            display: grid;
            padding: 0px;
            grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr;
            grid-gap: 15px;
            list-style-type: none;

            li {
                font-size: 16px;
                width: 100%;

                &:last-child{
                    margin-right: 0px;
                    &:after {
                        display: block;
                        content: "";
                        position: absolute;
                        margin: -113px 0px 0px 64px;
                        padding: 25px;
                        background: url('/images/slider-promotion/free-daily-spain.png') no-repeat;
                        background-size: contain;
                        animation: blink 1.2s step-start 0s infinite;
                        -webkit-animation: blink 1.2s step-start 0s infinite
                    }
                    @extend .keyframes;
                }
                .hot-game {
                    &:after {
                        display: block;
                        content: "";
                        position: absolute;
                        margin: -67px 0px 0px 32px;
                        padding: 32px;
                        background: url(/images/navbar-logo/hot-game-image.png) no-repeat;
                        background-size: contain;
                    }
                }

                .link {
                    @extend .border-radius-3px;
                    @extend .nav-image-bg;
                    @extend .border-style;
                    padding: 48px 15px 32px 15px;

                    div {
                        @extend .color-white;
                        @extend .display-inline-block;
                        height: 64px;
                        background: url(/images/navbar-logo/navbar-image.png) no-repeat;
                        width: 64px;
                        position: relative;
                        top: 5px;

                        span {
                            position: absolute;
                            bottom: -20px;
                            font-size: 11px;
                            font-weight: bold;
                            text-align: center;
                            right: -2px;
                            left: 0;
                            text-transform: uppercase;
                        }
                        .span-custom {
                            right: -14px;
                            left: -15px;
                        }
                    }
                }

                .link-padding { .images { background: url(/images/navbar-logo/09-lucky-spin.png) no-repeat;} } }

                .item-hot-game { .link { div { background-position: 0px -5px; } } }
                
                .item-sports { .link { div { background-position: -67px -10px; } } }
                
                .item-casino { .link { div { background-position: -131px -10px; } } }
                
                .item-slots { .link { div { background-position: -194px -7px; } } }
                
                .item-poker { .link { div { background-position: -2px -134px; } } }

                .item-arcade { .link { div { background-position: -130px -137px; } } }

                .item-togel { .link { div { background-position: -66px -133px; } } }

                .item-cock-fighter { .link { div { background-position: -191px -140px; } } }

                .item-lucky-spain {
                    .link-padding {
                        .lucky-spain-image {
                            @extend .border-radius-3px;
                            @extend .border-style;
                            background: url(/images/navbar-logo/9-lucky-spain.png) no-repeat;
                            padding: 50px;
                        }
                    }
                }
            }
        }
</style>