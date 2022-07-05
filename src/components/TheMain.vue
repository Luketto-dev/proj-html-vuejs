<template>
    <main>
        <!-- passo alla sezione come props l array che contine le informazioni per stampare la card -->
        <SectionMeetNewAgency :info-cards="avadaTeam"></SectionMeetNewAgency>
        <!-- passo alla sezione come props l array che contiene i nostri servizi per stamparli in una card -->
        <SectionOurServices :info-cards="infoCardsOurServices"></SectionOurServices>
        <!-- passo come props alla sezione gli url delle immagini che andrò a stampare  -->
        <SectionOurWorks :urls-images="urlsImagesOurWorks"></SectionOurWorks>
        <!-- passo come props alla sezione l array che contine i piani tariffari per poi stamparli in una card -->
        <SectionOurPlans :tariff-plans="tariffPlans"></SectionOurPlans>
        <!-- passo come props alla sezione l array che contine le nostre news per poi stamprle in una card -->
        <SectionOurNews :our-news="ourNews"></SectionOurNews>
        <SectionReviews></SectionReviews>
        <TheBanner></TheBanner>
    </main>
</template>

<script>
import SectionMeetNewAgency from './SectionMeetNewAgency.vue';
import SectionOurServices from './SectionOurServices.vue';
import SectionOurWorks from './SectionOurWorks.vue';
import SectionOurPlans from './SectionOurPlans.vue';
import SectionOurNews from './SectionOurNews.vue';
import SectionReviews from './SectionReviews.vue';
import TheBanner from './TheBanner.vue';

export default {
    data(){
        return{
            // mi salvo in un array la lista dei vari elementi checompongono le card da stampare
            avadaTeam:[
                {
                    iconClass: "fa-road",
                    title : "Establish Goals",
                    subtitle: "Aliquam non elit lacus. Praesent aliquet, Ipsum id scelerisque convallis, mi ligula euismod odio, vel dictum mi risus a mi."
                },
                {
                    iconClass: "fa-video",
                    title : "Work With a Team",
                    subtitle: "Cras semper auctor aliquam, Sed porta sed lacus sit amet consectetur. Lorem ipsum dolor sit amet, consectetur adipiscin."
                },
                {
                    iconClass: "fa-droplet",
                    title : "Get Results",
                    subtitle: "Vestibulum scelerisque egestas lectus sit amet molestie. Donec consectetur cursus est sed blandit. Nunc sed risus lacus."
                }
            ],
            // salvo in un array la lista dei servizi formati da elementi che stamperò in una card
            infoCardsOurServices:[
                {
                    iconClass: "fa-google",
                    title: "Google SEO",
                    subtitle : "Vestibulum in lacinia metus, Suspendisse in enim ipsum. nulla faciis. Donec ante turpis, dictum sed magna et, dapibus faucibus odio.",
                    linkText: "ReadMore",
                    iconPrefix: "fa-brands"
                },
                {
                    iconClass: "fa-gear",
                    title: "Brand Strategy",
                    subtitle : "Vestibulum in lacinia metus, Suspendisse in enim ipsum. nulla faciis. Donec ante turpis, dictum sed magna et, dapibus faucibus odio.",
                    linkText: "ReadMore"
                },
                {
                    iconClass: "fa-building",
                    title: "Local SEO",
                    subtitle : "Vestibulum in lacinia metus, Suspendisse in enim ipsum. nulla faciis. Donec ante turpis, dictum sed magna et, dapibus faucibus odio.",
                    linkText: "ReadMore"
                },
                {
                    iconClass: "fa-chart-column",
                    title: "Seo Analysis",
                    subtitle : "Vestibulum in lacinia metus, Suspendisse in enim ipsum. nulla faciis. Donec ante turpis, dictum sed magna et, dapibus faucibus odio.",
                    linkText: "ReadMore"
                },
            ],
            // lista di url per stampare immagini
            urlsImagesOurWorks:[
                "case-study-gallery-3-1-400x300.jpg",
                "case-study-gallery-2-400x300.jpg",
                "case-study-gallery-1-1-400x300.jpg",
                "case-study-gallery-4-1-400x300.jpg",
                "case-study-gallery-5-1-400x300.jpg",
                "case-study-gallery-6-1-400x300.jpg",
            ],
            //salvo i piani tariffari che offriamo coi i prezzi
            tariffPlans:[
                {
                    type: "Standard",
                    price: 19,
                    pojects : "5 Projects",
                    storage: "5 GB Storage",
                    users: "Unlimited Users"
                },
                {
                    type: "Premium",
                    price: 29,
                    pojects : "10 Projects",
                    storage: "15 GB Storage",
                    users: "Unlimited Users"
                },
                {
                    type: "Professional",
                    price: 39,
                    pojects : "15 Projects",
                    storage: "30 GB Storage",
                    users: "Unlimited Users"
                },
                {
                    type: "Extreme",
                    price: 59,
                    pojects : "Unlimited Projects",
                    storage: "Unlimited Storage",
                    users: "Unlimited Users"
                },
            ],
            // salvo lista delle news 
            ourNews:[
                {
                    urlImage:"related-service-2-320x202.jpg",
                    title : "Why You Need A SEO Agency Now",
                    date: "November 1st, 2017",
                    paragraph: "ALorem ipsum sit amet, sonsectetur adipiscing elit. In et scelerisque sem. Nunc molestie neque augue, at gravida mi blandit"
                },
                {
                    urlImage:"related-service-4-320x202.jpg",
                    title : "SEO Tips For Your Startup",
                    date: "December 1st, 2018",
                    paragraph: "ALorem ipsum sit amet, sonsectetur adipiscing elit. In et scelerisque sem. Nunc molestie neque augue, at gravida mi blandit"
                },
                {
                    urlImage:"blog-post-6-320x202.jpg",
                    title : "Image Optimization For Your Site",
                    date: "January 1st, 2019",
                    paragraph: "ALorem ipsum sit amet, sonsectetur adipiscing elit. In et scelerisque sem. Nunc molestie neque augue, at gravida mi blandit"
                },
            ],
        }
    },
    components:{
    SectionMeetNewAgency,
    TheBanner,
    SectionOurServices,
    SectionOurWorks,
    SectionOurPlans,
    SectionOurNews,
    SectionReviews,
}

}
</script>

<style lang="scss" scoped>

</style>