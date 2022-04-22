<template>
    <div class="list-show">
        <div class="image-card">
            <ul class="menus">
                <li :class="customClassFirst"><a class="link" href="#"><div></div></a></li>
                <li :class="customClassSecond"><a class="link" href="#"><div></div></a></li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        customClassFirst: String,
        customClassSecond: String,
    },
}
</script>

<style lang="scss" amp-boilerplate>
     .list-show {
        .image-card {
            padding: 10px;

            .menus {
                display: grid;
                grid-template-columns: 1fr 1fr;
                grid-gap: 10px;
                list-style-type: none;
                padding: 0px;
                li {
                    a {
                        div {
                            background: url(/images/card/card-image.png) no-repeat;
                            height: 166px;
                            width: 166px;
                            @extend .border-bg-cr;
                            @extend .border-radius-3px;
                        }
                    }
                }
                .border-bg-cr {
                    border: 1px solid $color-white;
                }

                // hot-game
                .item-custom-hot-game-first {a { div { background-position: 0px 0px;  } }}
                .item-custom-hot-game-second {a { div { background-position: -170px 0px;  } }}
                
                //sport
                .item-custom-sports-first {a { div { background-position: -340px -2px; } }}
                .item-custom-sports-second {a { div { background-position: -509px 0px;  } }}
                
                //casino
                .item-custom-casino-first {a { div { background-position: 0px -169px;  } }}
                .item-custom-casino-second {a { div { background-position: -170px -169px; } }}
                
                //slots
                .item-custom-slots-first {a { div { background-position: -341px -170px; } }}
                .item-custom-slots-second {a { div { background-position: -510px -169px; } }}

                //Poker
                .item-custom-poker-first {a { div { background-position: 0px -339px; } }}
                .item-custom-poker-second {a { div { background-position: -169px -339px; } }}
                
                //Arcade
                .item-custom-arcade-first {a { div { background-position: -341px -340px; } }}
                .item-custom-arcade-second {a { div { background-position: -510px -339px; } }}
                
                //Togel
                .item-custom-togel-first {a { div { background-position: 0px -509px; } }}
                .item-custom-togel-second {a { div { background-position: -169px -509px;  } }}
                
                //Cock Fighting
                .item-custom-cock-fighting-first {a { div { background-position: -340px -511px; } }}
                .item-custom-cock-fighting-second {a { div { background-position: -510px -509px;  } }}
            }
        }
     }
</style>