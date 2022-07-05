<template>
    <section class="reviews">
        <div class="container">
            <div class="reviews-content">
                <h2 class="fw-bold pb-3">What Our Clients Say</h2>
                <img src="/images/testimonials-2.jpg" alt="">
                <div class="py-3 fst-italic">Ability proceeds from a fusion of skills, Knowledge, understanding and imagination, consolidated by experience</div>
                <div class="color-scorpion"><span class="fw-bold">Luis Desaivo, </span>CREO TECH</div>
            </div>
            <div class="reviews-partner d-flex justify-content-center pt-5">
                <div v-for="(urlPartnerImg, i) in urlPartnersImg" :key="i"  class="reviews-partner-img">
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
            urlPartnersImg:[
                "clients_partner_5-200x202.png",
                "clients_partner_6-200x202.png",
                "clients_partner_1-200x202.png",
                "clients_partner_2-200x202.png"
            ]
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