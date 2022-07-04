<template>
    <section class="our-works">
        <div class="container">
            <div class="our-works-text">
                <h2 class="fw-bold">Our orks</h2>
                <div class="color-scorpion">Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium dolormque laudantium.</div>
            </div>    
            <div class="our-works-cards">
                <div class="row row-cols-3">
                    <div v-for="(infoCard, i) in InfoCards" :key="i" class="col">
                        <PictureCard :info-card="infoCard"></PictureCard>
                    </div>
                </div>
            </div>
        </div>      
    </section>
</template>

<script>
import PictureCard from './PictureCard.vue'

export default {
    props:{
        InfoCards: Array
    },
    components:{
        PictureCard
    }
    

}
</script>

<style lang="scss" scoped>
.our-works{

    & .our-works-text{
        width: 40%;
        text-align: center;
        margin: 0 auto;
    }
}
</style>