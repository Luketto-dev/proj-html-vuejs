<template>
    <main>
        <SectionMeetNewAgency :info-cards="InfoCards"></SectionMeetNewAgency>
        <SectionOurServices :info-cards="infoCardsOurServices"></SectionOurServices>
        <SectionOurWorks :info-cards="InfoCardsOurWorks"></SectionOurWorks>
        <TheBanner></TheBanner>
    </main>
</template>

<script>
import SectionMeetNewAgency from './SectionMeetNewAgency.vue'
import SectionOurServices from './SectionOurServices.vue'
import SectionOurWorks from './SectionOurWorks.vue'
import TheBanner from './TheBanner.vue'
export default {
    data(){
        return{
            InfoCards:[
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
            infoCardsOurServices:[
                {
                    iconClass: "fa-google fa-brand",
                    title: "Google SEO",
                    subtitle : "Vestibulum in lacinia metus, Suspendisse in enim ipsum. nulla faciis. Donec ante turpis, dictum sed magna et, dapibus faucibus odio.",
                    linkText: "ReadMore"
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
            InfoCardsOurWorks:[
                "case-study-gallery-3-1-400x300.jpg",
                "case-study-gallery-2-400x300.jpg",
                "case-study-gallery-1-1-400x300.jpg",
                "case-study-gallery-4-1-400x300.jpg",
                "case-study-gallery-5-1-400x300.jpg",
                "case-study-gallery-6-1-400x300.jpg",
            ]
            
        }
    },
    components:{
        SectionMeetNewAgency,
        TheBanner,
        SectionOurServices,
        SectionOurWorks,
    }

}
</script>

<style lang="scss" scoped>

</style>