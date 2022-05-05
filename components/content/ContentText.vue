<template>
   <div class="square-small" >
        <amp-fit-text class="color-text" :width="width" :height="height"  max-font-size="13">
            {{ ContentText }}
        </amp-fit-text>
        <div class="link-text">
            <a href="https://www.w3schools.com">Baca selanjutnya</a>
        </div>
    </div>

</template>

<script>
export default {
   props: {
       width: String,
       height: String,
       ContentText: String,
   }
}
</script>

<style lang="scss" amp-boilerplate>
    .square-small {
        text-align: left;

        .color-text {
            color: $text-color-1;
        }
        
        .link-text {
            a {
                text-decoration: none;
                color: $text-red;
                font-size: 14px;
            }
        }
    }
</style>