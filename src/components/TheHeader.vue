<template>
    <div>
        <header>
            <div class="container">
                <div class="my-navbar d-flex align-items-center">
                    <div class="my-navbar-logo">
                        <img src="../../public/images/logo_seo_w_1x.png" alt="Logo Seo">
                    </div>
                    <div class="menu d-flex flex-grow-1 align-items-center">
                        <ul class="menu-list d-flex flex-grow-1 justify-content-end">
                            <!-- ciclo sulla lista dei link dell headear per stamparli in html -->
                            <li v-for="(link,i) in headerLinks" :key="i"  class="menu-list-item">
                                <a class="menu-list-item-link" href="#">
                                    {{link}}
                                </a>
                            </li>
                        </ul>
                        <div class="cta">
                            <button class="btn my-btn-warning">GET IN TOUCH NOW</button>
                        </div>
                    </div>
                </div>
            </div>
            <TheJumbotron></TheJumbotron>      
        </header>
        
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
            // salvo la lista dei link in un array per poi stamparli attraverso un ciclo
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
    background-image: url("../../public/images/1-hero-image.png");
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;  
}
.my-navbar{
    font-size: .9rem;
    & .my-navbar-logo{
        width: 125px;

        & img{
            width: 100%;
        }
    }

    & .menu{
        & .menu-list{
            margin: 0;
            padding: 0;
            list-style: none;

            & .menu-list-item{
                padding: .5rem 1rem
                
            }

            & .menu-list-item-link{
                text-decoration: none;
                padding: .5rem 1rem;
                color: var(--color-alabaster);
                display: block;
                transition: all .3 ease-in-out;

                &:hover{
                    color: var(--color-yellow-orange);
                }
            }
        }

        
    }
}
</style>