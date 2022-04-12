<template>
    <!-- <div class="button-style">
         <div class="row">
            <button>PROMOSI</button>
            <button >BONUS</button>
            <button >HADIAH</button>
        </div>
    </div> -->
    <div class="inner-grid-btn">
        <!-- <amp-img class="image-size" on="tap:lightbox1" role="button" tabindex="0" :src="imagePromosi" width="220" height="30"   />
        <amp-img class="image-size" on="tap:lightbox1" role="button" tabindex="0" :src="imageBonus" width="220" height="30"  /> 
        <amp-img class="image-size" on="tap:lightbox1" role="button" tabindex="0" :src="imageHadiah" width="220" height="30"  />  -->
       
        <button class="btn btn-color-promosi">PROMOSI</button>
        <button class="btn btn-color-bonus">BONUS</button>
        <button class="btn btn-color-hadiah">HADIAH</button>
    </div>
</template>

<script>
export default {
   
}
</script>

<style lang="scss">
    .inner-grid-btn {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        grid-gap: 5px;
        padding: 13px 10px;

        .btn {
            border: 1px;
            padding: 8px 15px 8px 10px;
            border-radius: 3px;
            font-weight: 600;
        }
        .btn-color-promosi {
            @extend .btn-bg-red;
            color: $color-white;
        }
        .btn-color-bonus {
            @extend .btn-bg-white;
        }
        .btn-color-hadiah {
            @extend .btn-bg-white;
        }
    }
</style>