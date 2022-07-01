<template>
    <div class="jumbotron text-white">
        <div class="container">
            <div class="jumbotron-content">
                <div class="row">
                    <div class="col-5">
                        <div class="jumbotron-text">
                            <div class="jumbotron-text-title fw-bold">
                                <h1>SEM Campigns Made Simple With Avada</h1>
                            </div>
                            <div class="jumbotron-text-subtitle pb-2">
                                <h6 class="">Lorem Ipsum dolor sit amet, consectetur adipiscing elit. Phasellus eu ornare erat. Curubitur pulvinar elit.</h6>
                            </div>
                            <div class="jumbotron-buttons">
                                <button class="btn btn-warning me-2">BUY AVADA NOW</button>
                                <button class="btn btn-primary">CONTACT US</button>
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
    background-image: url("../../public/images/1-hero-image.png");
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;

    & .jumbotron-content{
        & .jumbotron-text{
            margin-top: 18rem;
            margin-bottom: 18rem;
        }
    }
}
</style>