<template>
    <main>
        <SectionMeetNewAgency :info-cards="InfoCards"></SectionMeetNewAgency>
        <TheBanner></TheBanner>
    </main>
</template>

<script>
import SectionMeetNewAgency from './SectionMeetNewAgency.vue'
import TheBanner from './TheBanner.vue'
export default {
    data(){
        return{
            InfoCards:[
                {
                    iconClass: "fa-road",
                    title : "Establish Goals",
                    subtitle: "Aliquam non elit lacus. Praesent aliquet, Ipsum id scelerisque convallis, mi ligula euismod odio, vel dictum mi risus a mi"
                },
                {
                    iconClass: "fa-video",
                    title : "Work With a Team",
                    subtitle: "Cras semper auctor aliquam, Sed porta sed lacus sit amet consectetur. Lorem ipsum dolor sit amet, consectetur adipiscin "
                },
                {
                    iconClass: "fa-droplet",
                    title : "Get Results",
                    subtitle: "Vestibulum scelerisque egestas lectus sit amet molestie. Donec consectetur cursus est sed blandit. Nunc sed risus lacus"
                }
            ]
            
        }
    },
    components:{
        SectionMeetNewAgency,
        TheBanner,
    }

}
</script>

<style lang="scss" scoped>

</style>