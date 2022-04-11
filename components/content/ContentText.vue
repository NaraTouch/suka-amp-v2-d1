<template>
   <div class="square-small" >
        <amp-fit-text width="300" height="100" layout="responsive" max-font-size="16">
            Lorem ipsum dolor sit amet, has nisl nihil convenire et, vim at aeque
            inermis reprehendunt. Lorem ipsum dolor sit amet, has nisl nihil convenire
            et, vim at aeque inermis reprehendunt
        </amp-fit-text>
        <div class="link-text">
            <a href="https://www.w3schools.com">Baca selanjutnya</a>
        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style lang="scss">
    .square-small {
        text-align: left;
            .link-text {
            margin: 10px 0px;
            a {
                text-decoration: none;
                color: $btn-color-1;
            }
        }
    }
</style>