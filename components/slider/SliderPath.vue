<template>
    <!-- <div class="button-style">
         <div class="row">
            <button>PROMOSI</button>
            <button >BONUS</button>
            <button >HADIAH</button>
        </div>
    </div> -->
    <div class="inner-grid">
        <button>PROMOSI</button>
        <button >BONUS</button>
        <button >HADIAH</button>
    </div>
</template>

<script>
export default {
    
}
</script>

<style lang="scss">
    .inner-grid {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        grid-gap: 5px;
        // div {
        //     background: lightgreen;
        //     padding: 8px;
        // }
        button {
            padding: 8px 10px;
            margin: 15px 10px 0px 10px;
            // display: inline-block;
            max-width: 100%;
            width: auto;
            height: auto;
            line-height: 1.3em;
            // padding: 0.8em 12em;
            // margin-right: 1.3em;
            
             font-family: 'Poppins', sans-serif;
            font-size: 1em;
            font-weight: 700;
            
             color: #005af0;
             text-decoration: none;
            // text-align: center;
            
             border: 0;
             border-radius: 3px;
            // background-color: #fff;
            
             box-shadow: var(--box-shadow-1);
            // transition: 
            //     transform .3s cubic-bezier(.25,.1,.25,1),
            //     box-shadow .3s cubic-bezier(.25,.1,.25,1);
            
             cursor: pointer;
            &:hover {
                // transform: translateY(-.125em);
                color: $color-white;
                background-color: $btn-color-1;
             }
             //&:last-child {
            //     margin-right: 0em;
            // }
        }
    }
    // .button-style {
    //     background: $color-gray;
    //     .row {
    //         // margin-bottom: 1.5rem;
    //         padding: 10px;
    //     }
    //     .gradient {
    //         color: #fff;
    //         background: linear-gradient(225deg,#00dcc0 0,#005af0 75%);
    //     }
    //     button {
    //         display: inline-block;
    //         max-width: 100%;
    //         width: auto;
    //         height: auto;
    //         line-height: 1.3em;
    //         padding: 0.8em 12em;
    //         margin-right: 1.3em;
            
    //         font-family: 'Poppins', sans-serif;
    //         font-size: 1em;
    //         font-weight: 700;
            
    //         color: #005af0;
    //         text-decoration: none;
    //         text-align: center;
            
    //         border: 0;
    //         border-radius: 3px;
    //         background-color: #fff;
            
    //         box-shadow: var(--box-shadow-1);
    //         transition: 
    //             transform .3s cubic-bezier(.25,.1,.25,1),
    //             box-shadow .3s cubic-bezier(.25,.1,.25,1);
            
    //         cursor: pointer;
    //         &:hover {
    //             // transform: translateY(-.125em);
    //             color: $color-white;
    //             background-color: $btn-color-1;
    //         }&:last-child {
    //             margin-right: 0em;
    //         }
    //     }
    // }
    // @keyframes run {
    //     0% {
    //         transform: translateX(0px);
    //     }
    //     25% {
    //         transform: translateX(2em);
    //         opacity: 0;
    //     }
    //     50% {
    //         transform: translate(-5em);
    //     }
    //     100% {
    //         transform: translateX(0px);
    //     }
    // }
</style>