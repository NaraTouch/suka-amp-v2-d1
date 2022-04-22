<template>
    <div class="header-title">
        <div v-if="customComponent" class="custom-class">
            <ul class="menus">
                <li :class="customClass"><a class="link" href="#"><div></div></a></li>
            </ul>
        </div>

        <div v-else class="image">
            <amp-img alt="image" :src="imageTitle" :width="width" :height="height" />
        </div>

        <div class="title-card" :class="customClass">
            <span class="span-right">{{title}}</span>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        title: String,
        imageTitle: String,
        width: String, 
        height: String,
        customClass: String,
        customComponent: Boolean,
        customClass: String,
     }    
}
</script>

<style lang="scss" amp-boilerplate>
    .header-title {
        @extend .display-flex;
       
        .title-card {
            padding: 7px 0px 0px 5px;
            color: $text-color-1;
        }

        .custom {
            padding: 4px 0px 0px 10px;
        }

        .custom-class {
            .menus {
                list-style-type: none;
                padding: 0px;
                
                li {
                    a {
                        div {
                            background: url(/images/card/card-title-image.png) no-repeat;
                            height: 35px;
                            width: 42px;
                        }
                    }
                }

                .item-custom-hot-game { a { div { background-position: 0px -7px; } } }

                .item-custom-casino { a { div { background-position: -85px -4px; } } }

                .item-custom-poker { a { div { background-position: 0px -45px; } } }

                .item-custom-togel { a { div { background-position: -87px -45px; } } }

                .item-custom-sports { a { div { background-position: -42px -5px; } } }

                .item-custom-slots { a { div { background-position: -127px -5px; } } }

                .item-custom-arcade { a { div { background-position: -44px -46px; } } }

                .item-custom-cock-fighting { a { div { background-position: -128px -45px; } } }
            }
        }
    }
</style>