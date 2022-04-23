<template>
    <div class="running-image-item" >
        <div class="image-icon">
            <ul class="menu">
                <li :class="customClassFirst"><a href="#"><div></div></a></li>
            </ul>
        </div>

        <div class="loading-number">
            <loading-number />
        </div>

        <div class="image-icon">
            <ul class="menu">
                <li :class="customClassSecond"><a href="#"><div></div></a></li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    components: { 
      loadingNumber: () => import('../components/loadingNumber'),
    },
    props: {
        customClassFirst: String,
        customClassSecond: String,
    }
}
</script>

<style lang="scss" amp-boilerplate>
    .running-image-item {
        display: flex;

        .loading-number {
            margin-top: 3px;
        }

        .image-icon {
            .menu {
                list-style-type: none;
                padding: 0px;
                li {
                    a {
                        div {
                            background: url(/images/running-ig/running-image-icon.png) no-repeat;
                            width: 100px;
                            height: 30px;
                        }
                    }
                }
                
                .item-jackopt { a { div { background-position: 0px -3px; } } } 

                .item-idnlive { a { div { background-position: -105px -3px; } } } 

                .item-pg { a { div { background-position: 0px -33px; } } } 
            }
        }
    }
</style>

