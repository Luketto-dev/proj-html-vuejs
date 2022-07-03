<template>
  <section class="meet-new-agency">
    <div class="container">
        <div class="meet-new-agency-text text-center">
            <h2 class="fw-bold">Meet The New Agency SEO Template <br> From The Avada Team</h2>
            <div class="color-scorpion">Sed ut perspiciatis unde omnis iste natus error sit voluptatem <br> accusantium dolormque laudantium.</div>
        </div>
        <div class="meet-new-agency-cards pt-5 pb-2">
            <div class="row row-cols-3">
                <div v-for="(InfoCard, i) in InfoCards" :key="i" class="col ">
                    <!-- componente card -->
                    <SectionCard :info-card="InfoCard"></SectionCard>
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
        InfoCards: Array
    }

}
</script>

<style lang="scss" scoped>
.meet-new-agency{
    background-color: var(--color-alabaster);
    padding-bottom: 0;

    & .meet-new-agency-poster img{
        width: 100%;

    }
    
}



    
</style>