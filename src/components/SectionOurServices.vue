<template>
  <section class="our-services">
    <div class="container">
        <div class="our-services-text">
            <h2 class="fw-bold">See Our Top Notch Services</h2>
            <div>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium dolormque laudantium.</div>
        </div>
        <div class="our-services-cards pt-5">
            <div class="row row-cols-4">
                <!-- ciclo sui dati ricevuti dal main -->
                <div v-for="(infoCard, i) in infoCards" :key="i" class="col">
                    <!-- passo come prop alla section-card il singolo oggetto contenuto nell array ricevuto dal main -->
                    <SectionCard :info-card="infoCard"></SectionCard>
                </div>
            </div>
        </div>
    </div>
  </section>
</template>

<script>
import SectionCard from "./SectionCard.vue";
export default {
    props:{
        // salvo i dati ricevuti dal main
        infoCards:Array
    },
    components:{
        SectionCard
    }
}
</script>

<style lang="scss" scoped>
.our-services{
    background-color: var(--color-deep-cove);
    padding-top: 5rem;
    padding-bottom: 12rem;
    background-image: url("../../public/images/pattern_background.png");
    background-size: 100%;
    background-position: center;
    & .our-services-text{
        width: 40%;
        margin: 0 auto;
        text-align: center;
        color: var(--color-alabaster);
    }

    
}
</style>