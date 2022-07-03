<template>
    <footer class="text-center mt-5">
        <div class="footer-icon">
            <img src="../../public/images/logo_seo_1x.png" alt="">
        </div>
        <ul class="footer-list d-flex justify-content-center">
            <li v-for="(footerLink,i) in footerLinks" :key="i" class="footer-list-item">
                <a class="footer-list-item-link" href="#">{{footerLink}}</a>
            </li>
        </ul>
        <div class="copyright text-center text-muted">
            ©Copyright2012-2020 | Avada Theme by <span class="text-black">ThemeFusion</span> | All Rights Reserved | Powered by <span class="text-black">WordPress</span>
        </div>
        <div class="footer-icons d-flex justify-content-center">
            <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
            <a href="#"><i class="fa-brands fa-instagram"></i></a>
            <a href="#"><i class="fa-brands fa-twitter"></i></a>
            <a href="#"><i class="fa-brands fa-youtube"></i></a>
        </div>
    </footer>
</template>

<script>
export default {
    data(){
        return{
            footerLinks:[
                "Home",
                "Who We Are",
                "What We Do",
                "Wher We Work",
                "Careers",
                "News",
                "Get in Touch Now"
            ],
            
        }
    }
}
</script>

<style lang="scss" scoped>
footer{
    padding-bottom: 3rem;
    .footer-icon{
        padding-bottom: 2rem;
        & img{
            width: 125px;
        }
        
    }

    & .footer-list{
        list-style: none;
        margin: 0;
        padding: 0;

        & .footer-list-item{
            padding: .5rem;

            & .footer-list-item-link{
                text-decoration: none;
                padding: .5rem;
                color: black;
                font-size: .8rem;
            }
        }
    }

    & .copyright{
        font-size: .8rem;
        padding-top:3rem;
        padding-bottom: 1.2rem;
    }

    & .footer-icons{
        & a{
            padding: 1rem;
            font-size: 1.7rem;
            color: #5E5F64;
            display: block;
        }
    }
}
</style>