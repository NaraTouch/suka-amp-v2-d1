<template>
    <div class="running-text">
        <div class="heading-block bg-1">
            <div class="box-area">
                <span class="box num3"></span>
                <span class="box num2"></span> 
                <span class="box num1"></span>
            </div>
        </div>
    </div>
</template>

<script>
export default {
}
</script>

<style lang="scss" scoped>
    .running-text {
        margin: 0px 20px;
        .heading-block {
           padding: 10px 20px;
            border: 1px solid $border-color-1;
            border-radius: 40px;
            .text-center {
                text-align: center;
            }
        }
        .bg-1 {
            background-image: url(/images/slide-bar/image-1.jpg);
        }
    }

    .box-area {
        text-align: center;
    }
    .box-area span {
        color: #fff;
        padding: 0 10px;
    }
    .box {
        display: inline-block;
        overflow: hidden;
        height: 1em;
        line-height: 1em;
        font-weight: bold;
        font-size: 16px;
    }
    .box::after {
        position: relative;
        white-space: pre;
        content: "0\A 1\A 2\A 3\A 4\A 5\A 6\A 7\A 8\A 9";
    }
    .box.num1::after {
        animation: animate 1s steps(10) infinite;
    }
    .box.num2::after {
        animation: animate 10s steps(10) infinite;
    }
    .box.num3::after {
        animation: animate 100s steps(10) infinite;
    }
    @keyframes animate {
        0% {
            top: 0;
        }
        100% {
            top: -10em;
        }
    }


// running text

</style>