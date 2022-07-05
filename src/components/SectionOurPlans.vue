<template>
    <section class="our-plans">
        <div class="container">
            <div class="our-plans-text">
                <h2 class="fw-bold">Our Plans</h2>
                <div>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium dolormque laudantium.</div>
            </div>
            <div class="our-plans-cards pt-5">
                <div class="row row-cols-4">
                    <!-- ciclo sull array arrivato dal main -->
                    <div v-for="(tariffPlan,i) in tariffPlans" :key="i" class="col">
                        <!-- passo come props a ourPlansCard il singolo oggetto contenuto nell array -->
                        <OurPlansCard :tariff-plan="tariffPlan"></OurPlansCard>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import OurPlansCard from './OurPlansCard.vue'
export default {
    props:{
        // salvo i dati arrivati dal main
        tariffPlans: Array,
    },
    components:{
        OurPlansCard
    }

}
</script>

<style lang="scss" scoped>
.our-plans{
    background-image: url("../../public/images/background1.jpg");
    background-size: cover;
    background-position: top;

    & .our-plans-text{
        width: 40%;
        margin: 0 auto;
        text-align: center;
        color: white;
    }
}
</style>