<template>
    <div>
        <div class="running-dev">
        <!-- <p>This is a horizontally scrolling text without a marquee tag.</p> -->
            <div class="running-text">
                <div>
                    <hr />
                </div>
                 <div class="image-size">
                    <amp-img src="../images/images.jpg" width="100px" height="20px" alt="a non-existent image">
                    </amp-img>
                </div>
                <div class="heading-block bg-1">
                    <div class="text-loading">
                        <span>RP </span>
                    </div>
                    <div class="box-area">
                        <span class="box num3"></span>
                        <span class="box num2"></span> 
                        <span class="box num1"></span>
                    </div>
                </div>
                <div class="image-size">
                    <amp-img src="../images/images.jpg" width="100px" height="20px" alt="a non-existent image">
                    </amp-img>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
}
</script>

<style lang="scss" scoped>
    .running-dev {
        background-color: $color-black;
        color: $color-white;
        padding: 10px;
        border: 1px solid $border-color-1;
        border-radius: 15px;
        overflow: hidden;
        position: relative;
        .running-text {
            -moz-animation: marquee 15s linear infinite;
            -webkit-animation: marquee 15s linear infinite;
            animation: marquee 15s linear infinite;
            display: flex;
            hr {
                height: 100%;
                margin: 0px 10px;
                border: 1px solid $border-color-1;
            }
            .heading-block {
                margin: 0px 10px;
                background: #180278;
                display: inline-flex;
                .text-center {
                    // text-align: center;
                }
                .text-loading {
                    font-weight: bold;
                    font-size: 16px;
                    margin: -2px 10px 0px 0px;
                }
                .bg-1 {
                    // background-image: url(/images/slide-bar/image-1.jpg);
                }
                .box-area {
                    text-align: center;
                }
                .box-area span {
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
            }
             .image-size {
                 height: 20px;
            }
        }
        @-moz-keyframes marquee {
            0% {
                transform: translateX(100%);
            }
            100% {
                transform: translateX(-100%);
            }
        }
        @-webkit-keyframes marquee {
            0% {
                transform: translateX(100%);
            }
            100% {
                transform: translateX(-100%);
            }
        }
        @keyframes marquee {
            0% {
                -moz-transform: translateX(100%);
                -webkit-transform: translateX(100%);
                transform: translateX(100%)
            }
            100% {
                -moz-transform: translateX(-100%);
                -webkit-transform: translateX(-100%);
                transform: translateX(-100%);
            }
        }
    }
</style>