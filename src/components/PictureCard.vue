<template>
    <div class="picture-card">
        <div class="picture-card-img">
            <img :src="'/images/' + pictureCardUrlImage" alt="">
        </div>
        
        <div v-if="this.singleNews" class="picture-card-title">
            <h4 class="fw-bold">{{this.singleNews.title}}</h4>
        </div>
        <div v-if="this.singleNews" class="picture-card-date color-scorpion pb-2">
            {{this.singleNews.date}}
        </div>
        <div v-if="this.singleNews" class="picture-card-paragraph color-scorpion">
            {{this.singleNews.paragraph}}
        </div>
    </div>
</template>

<script>
export default {
    props:{
        // mi salvo il singolo url ricevuto dalla sezione OurWork
        urlImage: String,
        // mi salvo il singolo oggetto ricevuto dalla sezione ourNews
        singleNews : Object,
    },
    computed:{
        // funzione che mi ritorna l url dell imagine da inserie
        pictureCardUrlImage(){
            if (this.singleNews === undefined) {
                return this.urlImage
            }

            return this.singleNews.urlImage
        }
    }

}
</script>

<style lang="scss" scoped>
.picture-card{
    
    & .picture-card-img{
        aspect-ratio: 1/.7;
        overflow: hidden;

        & img{
        width: 100%;
        height: 100%;
        transition: all .4s ease-in-out;

            &:hover{
                cursor: pointer;
                transform: scale(1.1);
            }

        }
    }

    

    & .picture-card-title{
        color: var(--color-yellow-orange);
        padding-top: 1rem;
    }

    & .picture-card-date{
        font-size: .7rem;
    }
}
</style>