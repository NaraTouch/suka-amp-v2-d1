<template>
    <div class="Image-One-show">
        <div class="image-card">
            <ul class="menus">
                <li :class="customClass"><a class="link" href="#"><div></div></a></li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        customClass: String,
    }
}
</script>

<style lang="scss" amp-boilerplate>
    .Image-One-show {
        .image-card {
            .menus {
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
        }
    }
</style>