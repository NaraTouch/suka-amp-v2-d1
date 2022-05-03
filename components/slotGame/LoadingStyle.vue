<template>
     <div class="loading-container">
        <div class="loading-bar">
            <div class="loading-bar--progress">
                <span class="first"></span>
                <span></span>
                <span></span>
                <span></span>
                <span></span>
                <span></span>
                <span></span>
                <span></span>
                <span></span>
                <span></span>
                <span></span>
                <span class="last"></span>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" amp-boilerplate>
    .loading-style {
        .btn-loading-style {
            border: 0;
            background: transparent;
        }
        .loading-container {
            margin: 0px 0px 10px 5px;
        
            .clickbait {
                margin: 1em;
            }

            .loading-bar {
            width: 120px;
                background: #cecece;
                padding: 1px;
                border-radius: 2px;
                margin: auto;
                &--progress {
                    display: flex;
                    & span {
                        margin: 0px 1px 0px 0px;
                        border-radius: 3px;
                        flex-basis: 11%;
                        flex-grow: 1;
                        flex-shrink: 1;
                        height: 12px;
                        animation: FadeIn 0.5s ease;
                        transition: all 1s cubic-bezier(0.17, 0.67, 0.88, 0.17);
                        &:last-child {
                            margin: 0px 0px 0px 0px;
                        }
                        
                        &:first-child {
                            border-top-left-radius: 4px;
                            border-bottom-left-radius: 4px;
                        }
                        &:last-child {
                            border-top-left-radius: 4px;
                            border-bottom-left-radius: 4px;
                        }
                    }
                }
                
            }

            .by-jasper {
                position: absolute;
                bottom: 2em;
                right: 2em;
                
            }

            @keyframes FadeIn {
                0% {
                    opacity: 0;
                    transform: scale(0.1);
                    // background: rgba(131, 125, 217, 1);
                    background: rgb(238, 113, 113);
                    border-radius: 4px;
                }

                85% {
                    opacity: 1;
                    background: rgb(238, 113, 113);
                    background: linear-gradient(
                        180deg,
                        rgb(238, 113, 113) 0%,
                        rgb(238, 47, 47) 56%,
                        rgb(245, 5, 5) 100%
                    );
                    border-radius: 0;
                    border-top-right-radius: 8px;
                    border-bottom-right-radius: 8px;
                }
                100% {
                    transform: scale(1);
                    background: rgb(238, 113, 113);
                    background: linear-gradient(
                        180deg,
                        rgb(238, 113, 113) 0%,
                        rgb(238, 47, 47) 56%,
                        rgb(245, 5, 5) 100%
                    );
                    border-radius: 0px;
                }
            }
            @for $i from 1 through 12 {
                .loading-bar--progress span:nth-child(#{$i}n) {
                    animation-delay: #{$i * 0.15}s;
                    animation-iteration-count: 1;
                    animation-fill-mode: both;
                }
            }
        }
    }
</style>