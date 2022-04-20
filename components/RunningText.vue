<template>
    <div class="running-container">
        <div class="text">
            <!-- <span>
                <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="currentColor" class="bi bi-megaphone-fill" viewBox="0 0 16 16">
                    <path d="M13 2.5a1.5 1.5 0 0 1 3 0v11a1.5 1.5 0 0 1-3 0v-11zm-1 .724c-2.067.95-4.539 1.481-7 1.656v6.237a25.222 25.222 0 0 1 1.088.085c2.053.204 4.038.668 5.912 1.56V3.224zm-8 7.841V4.934c-.68.027-1.399.043-2.008.053A2.02 2.02 0 0 0 0 7v2c0 1.106.896 1.996 1.994 2.009a68.14 68.14 0 0 1 .496.008 64 64 0 0 1 1.51.048zm1.39 1.081c.285.021.569.047.85.078l.253 1.69a1 1 0 0 1-.983 1.187h-.548a1 1 0 0 1-.916-.599l-1.314-2.48a65.81 65.81 0 0 1 1.692.064c.327.017.65.037.966.06z"/>
                </svg>
            </span> -->

            <title-image :image-title="titleIcon" :width="width" :height="height" />
            
        </div>
        <div class="marquee-container">
            <div class="marquee d-flex justify-content-around">
                <span>Lorem ipsum dolor sit amet consectetur adipisicing elit. Enim debitis blanditiis corrupti minus commodi vel ab nihil architecto doloremque, dolorem, eos, assumenda dicta dolor quos. Ratione repellendus corrupti molestias laborum!</span>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        components: {
            TitleImage: () => import('../components/TitleImage'),
        },
        data() {
            return {
                titleIcon: "/images/card/running-text-logo.png",
                width: "30",
                height: "25",
            }
        },
    }
</script>

<style lang="scss" >
    .running-container {
        @extend .border-radius-3px;
        @extend .display-flex;
        background-color: $bg-gray-contain;

        .text {
            margin: 10px 0px 10px 10px;
            
            span {
                svg{ 
                    fill:  $color-white; 
                }
            }
        }
        .marquee-container {
            @extend .border-radius-3px;
            @extend .display-flex;
            overflow: hidden;
            padding: 15px 0px;
            margin: 0px 0px;
            
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
            span { 
                @extend .color-white;
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
    }
</style>