<template>
    <div>
        <div class="position-relative marquee-container d-none d-sm-block">
            <div class="marquee d-flex justify-content-around">
                <span>Lorem ipsum dolor sit amet consectetur adipisicing elit. Enim debitis blanditiis corrupti minus commodi vel ab nihil architecto doloremque, dolorem, eos, assumenda dicta dolor quos. Ratione repellendus corrupti molestias laborum!</span>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>
    span { 
        color: $color-white;
    }
    .marquee-container {
        overflow: hidden;
        // line-height: 30px;
        // background: $color-gray;
        background-image: $background-image;
        background-repeat: no-repeat;
        padding: 10px;
        margin: 0px 0px;
        border-radius: 2px;
        display: inline-grid;
        .marquee {
            left: 100%;
            width: 100%;
            overflow: hidden;
            position: relative;
            white-space: nowrap;
            animation: marquee 15s linear infinite;
        }

        .marquee2 {
            animation-delay: 5s;
        }
    }

    @keyframes marquee {
        0% {
            left: 100%;
        }
        100% {
            left: -100%
        }
    }
</style>