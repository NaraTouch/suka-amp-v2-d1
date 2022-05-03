<template>
    <footers :hide="hide" />
</template>

<script>
    export default {
        props: {
            hide: Boolean
        },
        components: { 
            Footers: () => import('../Footers'), 
        },
    }
</script>

<style lang="scss" amp-boilerplate>
    
</style>