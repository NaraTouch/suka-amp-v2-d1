<template>
    <div class="header-title">
        <div v-if="customComponent" :class="CustomClassStyle ? 'custom-class-pr' : 'custom-class-no-pr'">
            <ul class="menus">
                <li :class="customClass"><a class="link" href="#"><div></div></a></li>
            </ul>
        </div>

        <div v-else class="image">
            <amp-img alt="image" :src="imageTitle" :width="width" :height="height" />
        </div>

        <div :class="hrContainerTitle"></div>
        
        <div class="title-card" :class="CustomClassStyle ? 'custom-class-pr' : 'custom-class-no-pr'">
            <span  >{{title}}</span>
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
            width: 4px;
        }

        .custom-class-pr {
            margin: 5px 5px;
            @extend .custom-class;

            span {
                font-size: 22px;
                font-weight: 100;
            }
        }
        
        .custom-class-no-pr {
            @extend .custom-class;
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