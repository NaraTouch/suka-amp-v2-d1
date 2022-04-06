<template>
    <div class="column-container">
        <section>
            <section>
                <Card />
                <Card />
                <Card />
                <Card />
            </section>
        </section>
        <section>
            <section>
                <Card />
                <Card />
                <Card />
                <Card />
            </section>
            
        </section>
        
    </div>
</template>

<script>
export default {
    data() {
        return {
            Card: () => import('../card/Card'),
        }
    },
}
</script>

<style lang="scss">
    .column-container {
            // margin-top: 30px;
        }
        
        .column-container>section>section>* {
            margin-bottom: 20px;
        }
        
        @media (min-width:400px) {
            .column-container {
                display: flex;
                margin: -22px -10px 0 -10px;
            }
            .column-container>section {
                width: 50%;
                margin: 0 10px;
            }
            @media (min-width:600px) {
                .column-container>section {
                    display: flex;
                    margin: 0;
                }
                .column-container>section>section {
                    width: 100%;
                    margin: 0 10px;
                }
            }
        }
</style>