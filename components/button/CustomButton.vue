<template>
    <div class="custom-buttom">
        <button>Lihat semuna</button>
    </div>
</template>

<script>
export default {
    
}
</script>
<style lang="scss">
    .custom-buttom {
        button {
        display: inline-block;
        max-width: 100%;
        width: auto;
        height: auto;
        line-height: 1.3em;
        padding: 0.8em 7em;
        margin-right: 0.3em;
        
        font-family: 'Poppins', sans-serif;
        font-size: 1em;
        font-weight: 700;
        
        color: #005af0;
        text-decoration: none;
        text-align: center;
        
        border: 0;
        border-radius: 3px;
        background-color: #fff;
        
        box-shadow: var(--box-shadow-1);
        transition: 
            transform .3s cubic-bezier(.25,.1,.25,1),
            box-shadow .3s cubic-bezier(.25,.1,.25,1);
        
        cursor: pointer;
            &:hover {
                // transform: translateY(-.125em);
                color: $color-white;
                background-color: $btn-color-1;
            }
        }
    }
</style>