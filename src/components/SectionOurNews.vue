<template>
    <section class="our-news">
        <div class="container">
            <div class="our-news-text pb-5">
                <h2 class="fw-bold">Our News</h2>
                <div class="color-scorpion">Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium dolormque laudantium.</div>
            </div>
            <div class="our-news-cards pb-5">
                <div class="row row-cols-3">
                    <!-- ciclo sull array ricevuto dal main -->
                    <div v-for="(singleNews, i) in ourNews" :key="i" class="col">
                        <!-- passo come props a pictureCard il singolo oggetto contenuto nell array ourNews -->
                        <PictureCard :single-news="singleNews"></PictureCard>
                    </div>
                </div>
            </div>
            <div class="our-news-button">
                <button class="btn my-btn-warning">GO TO NEWS</button>
            </div>
        </div>
    </section>
</template>

<script>
import PictureCard from './PictureCard.vue';
export default {
    components: {
        PictureCard,
    },
    props:{
        // salvo l array ricevuto dal main
        ourNews: Array,
    }
}
</script>

<style lang="scss" scoped>
.our-news{
    text-align: center;
    background-color: var(--color-alabaster);

    & .our-news-text{
        width: 40%;
        margin: 0 auto;
    }
}
</style>

