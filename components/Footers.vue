<template>
    <div class="footer">
        <div class="footer-image">
            <amp-img alt="image" :src="image" height="27" layout="fixed-height" />
        </div>
        <div v-if="hide" class="width-test">
            <action-connection />
        </div>
    </div>
</template>

<script>
    export default {
        props: {
            hide: Boolean,
        },
        components: {
            ActionConnection: () => import('../components/action/ActionConnection'),
        },
        data() {
            return {
                image: "/images/footer/footer-ig.png"
            }
        },
    }
</script>
<style lang="scss" amp-boilerplate>
    .footer {
        .footer-image {
            width: 45%;
        }
        .width-test {
            width: 1024px;
        }
    }
</style>