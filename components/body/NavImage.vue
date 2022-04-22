<template>
    <div class="navbar-images">
        <ul class="menus">
            <li class="item-hot-game"><a class="link" href="#"><div><span>Hot Game</span></div></a></li>
            <li class="item-sports"><a class="link" href="#"><div><span>Sports</span></div></a></li>
            <li class="item-casino"><a class="link" href="#"><div><span>Casino</span></div></a></li>
            <li class="item-slots"><a class="link" href="#"><div><span>Slots</span></div></a></li>
            <li class="item-poker"><a class="link" href="#"><div><span>Poker</span></div></a></li>
            <li class="item-arcade"><a class="link" href="#"><div><span>Arcade</span></div></a></li>
            <li class="item-togel"><a class="link" href="#"><div><span>Togel</span></div></a></li>
            <li class="item-cock-fighter"><a class="link" href="#"><div><span class="span-custom" >Cock Fighter</span></div></a></li>
            <li class="item-lucky-spain"><a class="link-padding" href="#"><div class="lucky-spain-image"></div></a></li>
        </ul>
    </div>
</template>

<script>
    export default {
    
    }
</script>

<style lang="scss" amp-boilerplate>
    .navbar-images {
        .hot-game {
            &:after {
                display: block;
                content: "";
                position: absolute;
                margin: -68px 0px 0px 32px;
                padding: 32px;
                background: url(/images/navbar-logo/hot-game-image.png) no-repeat;
                background-size: contain;
            }
        }
        .menus {
            list-style-type: none;
            display: grid;
            padding: 0px;
            grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr;
            grid-gap: 15px;

            li {
                font-size: 16px;
                font-family: "Trebuchet MS", Arial, sans-serif;
                width: 100%;

                &:first-child {
                    @extend .hot-game;
                }

                &:last-child{
                    margin-right: 0px;
                    @extend .free-daily-spain;
                }

                .link {
                    @extend .border-radius-3px;
                    @extend .nav-image-bg;
                    border: 1px solid $color-white;
                    padding: 48px 15px 32px 15px;

                    div {
                        @extend .color-white;
                        height: 64px;
                        display: inline-block;
                        background: url(/images/navbar-logo/navbar-image.png) no-repeat;
                        width: 64px;
                        position: relative;
                        top: 5px;

                        span {
                            position: absolute;
                            bottom: -20px;
                            font-size: 12px;
                            font-weight: bold;
                            text-align: center;
                            right: 0;
                            left: 0;
                            text-transform: uppercase;
                        }
                        .span-custom {
                            right: -12px;
                            text-align: unset;
                            left: -9px;
                        }
                    }
                }

                .link-padding { .images { background: url(/images/navbar-logo/09-lucky-spin.png) no-repeat;} } }

                .item-hot-game { .link { div { background-position: 0px -5px; } } }
                
                .item-sports { .link { div { background-position: -67px -10px; } } }
                
                .item-casino { .link { div { background-position: -131px -10px; } } }
                
                .item-slots { .link { div { background-position: -194px -7px; } } }
                
                .item-poker { .link { div { background-position: -2px -134px; } } }

                .item-arcade { .link { div { background-position: -66px -133px; } } }

                .item-togel { .link { div { background-position: -130px -137px; } } }

                .item-cock-fighter { .link { div { background-position: -191px -140px; } } }

                .item-lucky-spain {
                    .link-padding {
                        .lucky-spain-image {
                            @extend .border-radius-3px;
                            background: url(/images/navbar-logo/9-lucky-spain.png) no-repeat;
                            padding: 50px;
                            border: 1px solid $color-white;
                        }
                    }
                }
            }
        }
</style>