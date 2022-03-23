<template>
    <div id="navigation">
       <amp-list
            width="auto"
            height="30"
            layout="fixed-height"
            src="/static/inline-examples/data/amp-list-urls.json"
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
                    url: 'https://www.w3schools.com/'
                },
                {
                    title: 'Baccarat',
                    url: 'http://localhost:3000/'
                },
                {
                    title: 'Sports',
                    url: 'http://localhost:3000/'
                },
                {
                    title: 'Casino',
                    url: 'http://localhost:3000/'
                },
                {
                    title: 'Slots',
                    url: 'http://localhost:3000/'
                },
                {
                    title: 'Poker',
                    url: 'http://localhost:3000/'
                },
                {
                    title: 'Togel',
                    url: 'http://localhost:3000/'
                },
                {
                    title: 'Arcade',
                    url: 'http://localhost:3000/'
                },
                {
                    title: 'Cock Fighter',
                    url: 'http://localhost:3000/'
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