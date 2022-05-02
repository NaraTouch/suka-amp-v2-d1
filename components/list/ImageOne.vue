<template>
    <div class="Image-One-show">
        <div class="image-card">
            <ul :class="customimageClassStyle">
                <li :class="customClass"><a class="link" href="#"><div></div></a></li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        customClass: String,
        customimageClassStyle: String,
    },
    data() {
        return {
            
        }
    },
}
</script>

<style lang="scss" amp-boilerplate>
    .Image-One-show {
        
        // custom li
        .li-style {
            list-style-type: none;
            padding: 0px;
        }

        // custom border
        .border-style {
            border: 1px solid $color-white;
        }

        .image-card {
            .menus-hot-game {
                @extend .li-style;

                li {
                    a {
                        div {
                            @extend .border-radius-3px;
                            @extend .border-right;
                            @extend .border-style;
                            @extend .border-style;
                            background: url(/images/card/casino-image-new.png) no-repeat;
                            height: 240px;
                            width: 176px;
                        }
                    }
                }
                .maxbet-image { a { div { background-position: -2px 0px; } } }

                .co9-sport-image {a { div { background-position: -198px 0px; } }}

                .cmd-368-image { a { div { background-position: -2px -254px; } } }

                .pragmatic-play { a { div { background-position: -198px -253px; } } }
                
                .sbobet { a { div { background-position: -198px -254px; } } }
            }

            .menus-sport {
                @extend .li-style;
                li {
                    a {
                        div {
                            @extend .border-radius-3px;
                            @extend .border-right;
                            @extend .border-style;
                            background: url(/images/card/casino-image-new.png) no-repeat;
                            height: 240px;
                            width: 176px;
                        }
                    }
                }
                .maxbet-image { a { div { background-position: -2px 0px; } } }

                .co9-sport-image {a { div { background-position: -198px 0px; } }}

                .cmd-368-image { a { div { background-position: -2px -254px; } } }

                .pragmatic-play { a { div { background-position: -198px -253px; } } }
                
                .sbobet { a { div { background-position: -198px -254px; } } }
            }
            
            .menus-casino {
                @extend .li-style;
                li {
                    a {
                        div {
                            @extend .border-radius-3px;
                            @extend .border-right;
                            background: url(/images/card/casino-image-use.png) no-repeat;
                            height: 223px;
                            width: 188px;
                        }
                    }
                }
                .maxbet-image { a { div { background-position: 7px 0px; } } }

                .co9-sport-image { a { div { background-position: -187px 0px; } } }

                .cmd-368-image { a { div { background-position: -376px 0px; } } }

                .ho-gaming { a { div { background-position: -570px 0px; } } }

                .dream-gaming { a { div { background-position: -766px 0px; } } }

                .green-dragon { a { div { background-position: 6px -232px; } } }

                .ww-casino { a { div {  background-position: -186px -232px; } } }

                .icon-casino { a { div { background-position: -376px -232px; } } }

                .pragmatic-play { a { div { background-position: -580px -232px; } } }

                .sbobet { a { div { background-position: -767px -232px; } } }
            }

             .menus-togel {
                @extend .li-style;
                li {
                    a {
                        div {
                            @extend .border-radius-3px;
                            @extend .border-right;
                            background: url(/images/card/casino-image-use.png) no-repeat;
                            height: 223px;
                            width: 188px;
                        }
                    }
                }
                .s1288-image { a { div { background-position: 3px 0px; } } }

                .sv388-image { a { div { background-position: -191px 0px; } } }
            }

            .menus-arcade {
                @extend .li-style;
                li {
                    a {
                        div {
                            @extend .border-radius-3px;
                            @extend .border-right;
                            @extend .border-style;
                            background: url(/images/card/casino-image-new.png) no-repeat;
                            height: 240px;
                            width: 176px;
                        }
                    }
                }

                .forture-fishing-image { a { div { background-position: 0px 0px; } } }

                .fish-catch-image { a { div { background-position: 0px 0px; } } }

                .fish-king-image { a { div { background-position: 0px 0px; } } }

                .paradrse-play { a { div { background-position: 0px 0px; } } }

                .fishing-war-play { a { div { background-position: 0px 0px; } } }
            }

            .menus-cock-fighting {
                @extend .li-style;
                li {
                    a {
                        div {
                            @extend .border-radius-3px;
                            @extend .border-right;
                            @extend .border-style;
                            background: url(/images/card/casino-image-new.png) no-repeat;
                            height: 240px;
                            width: 176px;
                        }
                    }
                }
                
                .s1288-image { a { div { background-position: 0px 0px; } } }

                .sv388-image { a { div { background-position: -198px 0px; } } }
            }

            .menus-slots {
                 @extend .li-style;
                li {
                    a {
                        div {
                            @extend .border-radius-3px;
                            @extend .border-right;
                            @extend .border-style;
                            background: url(/images/card/slots-game-image.png) no-repeat;
                            height: 120px;
                            width: 120px;
                        } 
                    }
                }
                .game-image { a { div { background-position: 0px 0px; } } }
            }
       }
    }
</style>