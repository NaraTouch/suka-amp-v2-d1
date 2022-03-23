<template>
    <div id="navigation">
       <amp-list
            width="auto"
            height="30"
            layout="fixed-height"
            class="nav-responsive"
            >
            <template type="amp-mustache">
                <div class="url-entry" v-for="item in items">
                    <a :href="item.url">{{item.title}}</a>
                </div>
            </template>
        </amp-list>
    </div>
</template>

<script>
export default {
    data() {
        return {
            items: [
                {
                    title: 'Home',
                    url: '/'
                },
                {
                    title: 'bandar-baccarat',
                    url: '/bandar-baccarat'
                },
                {
                    title: 'Sports',
                    url: '/sports'
                },
                {
                    title: 'Casino',
                    url: '/casino'
                },
                {
                    title: 'Slots',
                    url: '/slots'
                },
                {
                    title: 'Poker',
                    url: '/pokers'
                },
                {
                    title: 'Togel',
                    url: '/togels'
                },
                {
                    title: 'Cock Fighter',
                    url: '/cock-fights'
                },
            ]
        }
    },
}
</script>

<style lang="scss" scoped>
    #navigation {
        margin: 10px;
        .nav-responsive {
            display: flex;
            .url-entry {
                margin: 5px 14px;
                a {
                    text-decoration: none;
                    color: $text-color-1;
                }
            }
        }
        @media #{$sm-device} {
            .nav-responsive {
                &:first-of-type {
                    visibility: visible;
                }
                &:last-of-type {
                    visibility: hidden;
                }
            }
        }
    }
</style>