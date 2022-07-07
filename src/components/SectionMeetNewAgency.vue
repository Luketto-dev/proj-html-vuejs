<template>
  <section class="meet-new-agency">
    <div class="container">
        <div class="meet-new-agency-text">
            <h2 class="fw-bold">Meet The New Agency SEO Template From The Avada Team</h2>
            <div class="color-scorpion">Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium dolormque laudantium.</div>
        </div>
        <div class="meet-new-agency-cards pt-5 pb-2">
            <div class="row row-cols-3">
                <!-- ciclo selle informazioni ricevute dal main -->
                <div v-for="(infoCard, i) in infoCards" :key="i" class="col ">
                    <!-- passo come props il singolo oggetto contenuto all interno dell array ricevuto dal main -->
                    <SectionCard :info-card="infoCard"></SectionCard>
                </div>
            </div>
        </div>
        <div class="meet-new-agency-poster">
            <img src="../../public/images/agency-seo-desk-front-1200x570.jpg" alt="">
        </div>
        
    </div>
  </section>
</template>

<script>
import SectionCard from "./SectionCard.vue";

export default {
    components:{
        SectionCard,
    },
    data(){
        return{
            

        }
    },
    props:{
        // mi salvo come props le informazioni ricevute dal main
        infoCards: Array
    }

}
</script>

<style lang="scss" scoped>
.meet-new-agency{
    background-color: var(--color-alabaster);
    padding-bottom: 0;

    & .meet-new-agency-text{
        width: 40%;
        margin: 0 auto;
        text-align: center;
    }

    & .meet-new-agency-poster img{
        width: 100%;

    }
    
}



    
</style>