<template>
    <div class="container">
        <amp-carousel height="200" layout="fixed-height" type="carousel"> 
            <amp-img src="https://amp.dev/static/samples/img/image1.jpg" width="400" height="300" alt="a sample image"></amp-img> 
            <amp-img src="https://amp.dev/static/samples/img/image2.jpg" width="400" height="300" alt="another sample image"></amp-img> 
            <amp-img src="https://amp.dev/static/samples/img/image1.jpg" width="400" height="300" alt="a sample image"></amp-img> 
            <amp-img src="https://amp.dev/static/samples/img/image3.jpg" width="400" height="300" alt="and another sample image"></amp-img>
            <amp-img src="https://amp.dev/static/samples/img/image1.jpg" width="400" height="300" alt="a sample image"></amp-img> 
            <amp-img src="https://amp.dev/static/samples/img/image3.jpg" width="400" height="300" alt="and another sample image"></amp-img>
            <amp-img src="https://amp.dev/static/samples/img/image1.jpg" width="400" height="300" alt="a sample image"></amp-img> 
            <amp-img src="https://amp.dev/static/samples/img/image3.jpg" width="400" height="300" alt="and another sample image"></amp-img>
        </amp-carousel>
    </div>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>
    img{
        width:100%;
        max-width:100%;
        height:auto;
        margin-bottom:15px;
        transition:all .9s
    }

    .container {
    max-width: 100%;
    margin: 4% auto;
    padding: 20px;
    color: #222;
    font-size: 16px;
    line-height: 1.6;
    box-shadow:0 2px 5px 0 rgba(0,0,0,0.16),0 2px 10px 0 rgba(0,0,0,0.12);
    border-radius: 8px;
    }

    .blue-box, .green-box, .red-box {
        width: 100%;
        height: 280px;
    }

    .blue-box {
        background: #00f;
    }

    .green-box {
        background: green;
    }
    
    .red-box {
        background: red;
    }

</style>