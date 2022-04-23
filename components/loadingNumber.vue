<template>
    <div class="heading-block">
        <div class="text-loading">
            <span>RP </span>
        </div>
        <div class="box-area">
            <span class="box num3"></span>
            <span class="box num2"></span> 
            <span class="box num1"></span>
        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" amp-boilerplate>
    .heading-block {
        @extend .display-flex;
        margin: 0px 10px;
        // background: #180278;

        .text-loading {
            font-weight: bold;
            font-size: 16px;
            margin: 0px 5px 0px 0px;
            background: #180278;
            padding: 2px 4px 2px 4px;
        }
        
        .box-area {
            @extend .display-flex;
            background: #180278;
            padding: 3px 4px 0px 4px;
        }
        
        .box {
            @extend .display-inline-block;
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
    }
</style>