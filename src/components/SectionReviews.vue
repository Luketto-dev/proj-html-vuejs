<template>
    <section class="reviews">
        <div class="container">
            <div class="reviews-content">
                <h2 class="fw-bold pb-3">What Our Clients Say</h2>
                <img :src="'/images/' + testimonials[indexTestimonial].urlImg" alt="">
                <div class="py-3 fst-italic">{{testimonials[indexTestimonial].review}}</div>
                <div class="color-scorpion"><span class="fw-bold">{{testimonials[indexTestimonial].name}}, </span>{{testimonials[indexTestimonial].job}}</div>
                <div class="reviews-button pt-3 d-flex justify-content-center">
                    <div class="me-3" :class="this.indexTestimonial === 0 ? 'bg-dark': ''" @click="changeActiveTestimonail('prev')"></div>
                    <div class="" :class="this.indexTestimonial === 1 ? 'bg-dark': ''" @click="changeActiveTestimonail('next')"></div>
                </div>
            </div>
            <div class="reviews-partner d-flex justify-content-center pt-5">
                <!-- ciclo sull array  -->
                <div v-for="(urlPartnerImg, i) in urlPartnersImg" :key="i"  class="reviews-partner-img">
                    <!-- stampo le immagini attraverso un cilo  -->
                    <img :src="'/images/' + urlPartnerImg" alt="">
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    data(){
        return{
            indexTestimonial: 0,
            testimonials:[
                {
                    urlImg: "testimonials-2.jpg",
                    review: "Ability proceeds from a fusion of skills, Knowledge, understanding and imagination, consolidated by experience",
                    name: "Luis Desavio",
                    job: "CREO TECH"
                },
                {
                    urlImg: "testimonials-1.jpg",
                    review: "Beauty is when you can appreciate yourself. When you love yourself, that’s when you’re most beautiful.",
                    name: "Shelia McCourtney",
                    job: "ARCHITECT"
                },
            ],
            // mi salvo in un array la url di ogni immagine
            urlPartnersImg:[
                "clients_partner_5-200x202.png",
                "clients_partner_6-200x202.png",
                "clients_partner_1-200x202.png",
                "clients_partner_2-200x202.png"
            ]
        }
    },
    methods:{
        changeActiveTestimonail(direction){
            if (direction === "next") {
                this.indexTestimonial = 1;

            }else if (direction === "prev") {
                this.indexTestimonial = 0;

        
            }
        }
    }

}
</script>

<style lang="scss" scoped>
.reviews{

    & .reviews-content{
        width: 35%;
        margin: 0 auto;
        text-align: center;

        & img{
        border-radius: 50%;
        }

    }

    & .reviews-button div{
        padding: .4rem;
        border: 1px solid black;
        border-radius: 50%;
        cursor: pointer;
    }

    & .reviews-partner{

        & .reviews-partner-img{
            padding: 3rem 6rem;

            & img{
                width: 80px;
            }
            
        }
    }
    

    
}
</style>