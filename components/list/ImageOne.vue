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
        .image-card {
            .menus-sport {
                list-style-type: none;
                padding: 0px;
                li {
                    a {
                        div {
                            @extend .border-radius-3px;
                            @extend .border-right;
                            border: 1px solid $color-white;
                            background: url(/images/card/card-image-sport.png) no-repeat;
                            height: 212px;
                            width: 154px;
                        }
                    }
                }
                .maxbet-image { a { div { background-position: -1px 0px; } } }

                .co9-sport-image {a { div { background-position: -158px 0px; } }}

                .cmd-368-image { a { div { background-position: -1px -222px; } } }

                .pragmatic-play { a { div { background-position: -158px -223px; } } }
            }
            
            .menus-casino {
                list-style-type: none;
                padding: 0px;
                li {
                    a {
                        div {
                            @extend .border-radius-3px;
                            @extend .border-right;
                            background: url(/images/card/casino-image-card.png) no-repeat;
                            height: 220px;
                            width: 178px;
                        }
                    }
                }
                .maxbet-image { a { div { background-position: 12px 0px; } } }

                .co9-sport-image { a { div { background-position: -151px 0px; } } }

                .cmd-368-image { a { div { background-position: -327px 0px; } } }

                .ho-gaming { a { div { background-position: -499px 0px; } } }

                .pragmatic-play { a { div { background-position: 12px -225px; } } }

                .green-dragon { a { div { background-position: -151px -225px; } } }

                .ww-casino { a { div { background-position: -327px -225px; } } }

                .icon-casino { a { div { background-position: -499px -225px; } } }
            }
        }
    }
</style>