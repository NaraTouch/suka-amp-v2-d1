<template>
    <div class="actions">
        <div></div>
        <div class="action-image">
            <ul class="menu">
                <li class="item-home"><a href="#"><div></div></a></li>
                <li class="item-profile"><a href="#"><div></div></a></li>
                <li class="item-bullets"><a href="#"><div></div></a></li>
                <li class="item-box"><a href="#"><div></div></a></li>
                <li class="item-chat"><a href="#"><div></div></a></li>
            </ul>
        </div>
    </div>
</template>

<script>
    export default {
    
    }
</script>

<style lang="scss" amp-boilerplate>

    .actions {
        @extend .display-grid;
        @extend .z-index-1;
        @extend .position-fixed;
        bottom: -1px;
        grid-template-columns: 2.693fr 1fr;
        
        .action-image {
            .menu {
                list-style-type: none;
                display: grid;
                padding: 0px;
                grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
                grid-gap: 0px;
                li {
                    a {
                        div {
                            background: url(/images/footer/action-image.png) no-repeat;
                            width: 55px;
                            height: 45px;
                        }
                    }
                }
                .item-home { a { div { background-position: 0px 1px; } } }

                .item-profile { a { div { background-position: -54px 1px; } } }
                
                .item-bullets { a { div { background-position: -107px 1px; } } }
                
                .item-box { a { div { background-position: 3px -45px; } } }
                
                .item-chat { a { div { background-position: -51px -45px; } } }
            }
        }
    }
</style>