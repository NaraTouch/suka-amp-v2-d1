<template>
    <div class="header-title">
        <div v-if="customComponent" :class="CustomClassStyle ? 'custom-class-pr' : 'custom-class-no-pr'">
            <ul class="menus" :class="customMenusStyle">
                <li :class="customClass"><a class="link" href="#"><div></div></a></li>
            </ul>
        </div>
<!-- 
        <div v-else class="image">
            <amp-img alt="image" :src="imageTitle" :width="width" :height="height" />
        </div> -->

        <div :class="hrContainerTitle"></div>
        
        <div class="title-card" :class="CustomClassStyle ? 'custom-class-pr' : 'custom-class-no-pr'">
            <span :class="spanStyle" >{{title}}</span>
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
        CustomClassStyle: Boolean,
        hrContainerTitle: String,
        customMenusStyle: String,
        spanStyle: String,
     }    
}
</script>

<style lang="scss" amp-boilerplate>
    .header-title {
        @extend .display-flex;
       
        .title-card {
            @extend .font-size;
            @extend .color-white;
            padding: 7px 0px 0px 5px;
        }

        .custom {
            padding: 4px 0px 0px 10px;
        }

        .hr-conatiner-title {
            background-image: url('/images/card/hr-container-sport.png');
            background-repeat: no-repeat;
            width: 3px;
            background-size: contain;
        }

        .hr-container-title-white {
            background-image: url('/images/card/hr-container-tab.png');
            background-repeat: no-repeat;
            width: 4px;
            background-size: contain;
        }

        .custom-class-pr {
             margin: 5px 10px;
            @extend .custom-class;

            span {
                font-size: 22px;
                font-weight: 100;
            }
            .span-style {
                @extend .span-font;
            }
        }
        
        

        .custom-class-no-pr {
            @extend .custom-class;

            .span-style {
                @extend .span-font;
            }
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

            .menus-tab {
                list-style-type: none;
                padding: 0px;
                li {
                    a {
                        div {
                            background: url(/images/card/tab-image-tab.png) no-repeat;
                            height: 42px;
                            width: 62px;
                        }
                    }
                }
                .item-custom-habanero { a { div { background-position: 9px 3px; } } }

                .item-custom-micro-gaming { a { div { background-position: -49px 2px; } } }

                .item-custom-pragmatic-play { a { div { background-position: -101px 1px; } } }

                .item-custom-pocket-games-soft { a { div { background-position: -157px 4px; } } }

                .item-custom-big-gaming { a { div { background-position: 8px -37px; } } }

                .item-custom-rtg-slots { a { div { background-position: -53px -36px; } } }

                .item-custom-joker-gaming { a { div { background-position: -128px -37px; } } }

                .item-custom-cq9-gaming { a { div { background-position: -128px -73px; } } }

                .item-custom-spade-gaming { a { div { background-position: 9px -74px; } } }

                .item-custom-flow-gaming { a { div { background-position: -51px -73px; } } }
            }
        }
    }
</style>