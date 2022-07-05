<template>
    <div class="jumbotron">
        <div class="container">
            <div class="jumbotron-content">
                <div class="row">
                    <div class="col-5">
                        <div class="jumbotron-text">
                            <div class="jumbotron-text-title pb-3">
                                <h1>SEM Campigns Made Simple With Avada</h1>
                            </div>
                            <div class="jumbotron-text-subtitle pb-3">
                                <h6 class="">Lorem Ipsum dolor sit amet, consectetur adipiscing elit. Phasellus eu ornare erat. Curubitur pulvinar elit.</h6>
                            </div>
                            <div class="jumbotron-buttons">
                                <button class="btn my-btn-warning me-2">BUY AVADA NOW</button>
                                <button class="btn my-btn-primary">CONTACT US</button>
                            </div>
                        </div>
                    </div>
                    <div class="col-7">
                        
                    </div>
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
.jumbotron{
    

    & .jumbotron-content{

        & .jumbotron-text{
            margin-top: 18rem;
            margin-bottom: 18rem;
            color: var(--color-alabaster);

            & .jumbotron-text-title h1{
                font-weight: 900;
                font-size: 3rem;

            }
        }
    }
}
</style>