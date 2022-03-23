<template>
    <div id="running-text">
        <div class="heading-block bg-1">
            <div class="text-center">
                 <!-- loading number -->
                <div class="loading-number"></div>
            </div>
            <div class="overlay"></div>
	    </div>
    </div>
</template>

<script>
export default {
   data() {
       return {
       }
   },
}
</script>

<style lang="scss" scoped>
    .loader {
    border: 16px solid #f3f3f3;
    border-top: 16px solid #3498db;
    border-radius: 50%;
    width: 36px;
    height: 36px;
    animation: spin 2s linear infinite;
    }

    @keyframes spin {
    0% {
        transform: rotate(0deg);
    }
    100% {
        transform: rotate(360deg);
    }
    }
    #running-text {
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
        .img-layout  {
            img {
                max-width: 1000px;
                max-height: 100px;
            }
        }
        .text-color {
            color: $color-white;
        }
    }
    // loading number
    @property --num {
    syntax: "<integer>";
    initial-value: 0;
    inherits: false;
    }

    .loading-number {
    animation: counter 5s infinite alternate ease-in-out;
    counter-reset: num var(--num);
    font: 800 40px system-ui;
    }
    .loading-number::after {
    content: counter(num);
    }

    @keyframes counter {
    from {
        --num: 0;
    }
    to {
        --num: 100;
    }
    }
</style>