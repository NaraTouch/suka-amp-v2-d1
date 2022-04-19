<template>
    <div class="footer">
        <div class="footer-image">
            <amp-img alt="image" :src="image" height="27" layout="fixed-height" />
        </div>
        <action-connection />
    </div>
</template>

<script>
    export default {
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
<style lang="scss">
    .footer {
        color: red;
        .footer-image {
            width: 45%;
        }
    }
</style>