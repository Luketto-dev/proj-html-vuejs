<template>
    <div class="picture-card">
        <img :src="'/images/' + pictureCardUrlImage" alt="">
        <div class="picture-card-title">
            <h4 class="fw-bold">{{pictureCardTitle}}</h4>
        </div>
        <div class="picture-card-date color-scorpion pb-2">
            {{pictureCardDate}}
        </div>
        <div class="picture-card-paragraph color-scorpion">
            {{pictureCardParagraph}}
        </div>
    </div>
</template>

<script>
export default {
    props:{
        urlImage: String,
        singleNews : Object,
    },
    computed:{
        pictureCardTitle(){
            if (this.singleNews === undefined) {
                return
            }

            return this.singleNews.title;
        },
        pictureCardDate(){
            if (this.singleNews === undefined) {
                return
            }
            return this.singleNews.date
        },
        pictureCardParagraph(){
            if (this.singleNews === undefined) {
                return
            }
            return this.singleNews.paragraph
        },
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
    aspect-ratio: 1/.7;

    & img{
        width: 100%;
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