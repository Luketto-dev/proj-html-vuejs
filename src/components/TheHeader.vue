<template>
    <div>
        <header>
            <div class="container">
                <div class="my-navbar d-flex align-items-center">
                    <div class="my-navbar-logo">
                        <img src="../../public/images/logo_seo_w_1x.png" alt="Logo Seo">
                    </div>
                    <div class="my-nav d-flex flex-grow-1 align-items-center">
                        <ul class="my-nav-list d-flex flex-grow-1 justify-content-end">
                            <li v-for="(link,i) in headerLinks" :key="i"  class="my-nav-list-item">
                                <a class="my-nav-list-item-link" href="#">
                                    {{link}}
                                </a>
                            </li>
                        </ul>
                        <div class="cta">
                            <button class="btn btn-warning">GET IN TOUCH NOW</button>
                        </div>
                    </div>
                </div>
            </div>      
        </header>
        <TheJumbotron></TheJumbotron>
</div>
</template>

<script>
import TheJumbotron from './TheJumbotron.vue'
export default {
    components:{
        TheJumbotron,
    },
    data(){
        return{
            headerLinks:[
                "Home",
                "Who We Are",
                "What We Do",
                "Where We Work",
                "Careers",
                "News",
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
header{
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
}
.my-navbar{
    font-size: .7rem;
    & .my-navbar-logo{
        width: 100px;

        & img{
            width: 100%;
        }
    }

    & .my-nav{
        & .my-nav-list{
            margin: 0;
            padding: 0;
            list-style: none;

            & .my-nav-list-item{
                padding: .5rem 1rem
                
            }

            & .my-nav-list-item-link{
                text-decoration: none;
                padding: .5rem 1rem;
                color: white;
                display: block;
            }
        }

        
    }
}
</style>