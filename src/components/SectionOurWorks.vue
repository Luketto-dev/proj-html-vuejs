<template>
    <section class="our-works">
        <div class="container">
            <div class="our-works-text pb-5">
                <h2 class="fw-bold">Our Works</h2>
                <div class="color-scorpion">Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium dolormque laudantium.</div>
            </div>    
            <div class="our-works-cards pb-5">
                <div class="row row-cols-3 gy-3">
                    <!-- ciclo sull array ricevuto dal main -->
                    <div v-for="(urlImage, i) in urlsImages" :key="i" class="col">
                        <!-- passo come props alla picturecard il singolo elemento all interno dell array ricevuto dal main -->
                        <PictureCard :url-image="urlImage"></PictureCard>
                    </div>
                </div>
            </div>
            <div class="our-works-button text-center">
                <button class="btn my-btn-warning">View Our Works</button>
            </div>
        </div>      
    </section>
</template>

<script>
import PictureCard from './PictureCard.vue'

export default {
    props:{
        // salvo i dati iviati dal main
        urlsImages: Array
    },
    components:{
        PictureCard,
        
    }
    

}
</script>

<style lang="scss" scoped>
.our-works{
     background-color: var(--color-alabaster);
    & .our-works-text{
        width: 40%;
        text-align: center;
        margin: 0 auto;
    }
}
</style>