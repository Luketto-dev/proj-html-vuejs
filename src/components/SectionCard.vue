<template>
  <div class="section-card" :class="infoCard.linkText ? 'bg-lucky-point' : 'bg-white'">
    <div><i :class="iconClass"></i></div>
    <div class="section-card-title">
        <h3 class="fw-bold pt-4">{{infoCard.title}}</h3>
    </div>
    <div class="section-card-subtitle pt-3" :class="infoCard.linkText ? 'color-alabaster' : 'color-scorpion'">
        {{infoCard.subtitle}}
    </div>
    <div v-if="infoCard.linkText" class="section-card-link pt-4">
        <a href="">{{infoCard.linkText}}</a>
    </div>
  </div>
</template>

<script>
export default {
    props:{
        // salvo l oggetto ricevuto dalla sezione
        infoCard : Object,
        
    },
    computed:{
        // funzione che ritorna le classi da aggiungere  alle icone
        iconClass(){
            let toReturn = "fa-solid"

            if (!this.infoCard) {
                return ''
            }

            if (this.infoCard && this.infoCard.iconPrefix) {
                toReturn = this.infoCard.iconPrefix


            }

            return toReturn + ' ' + this.infoCard.iconClass
        }
    }

}
</script>

<style lang="scss" scoped>

.bg-lucky-point{
    background-color: var(--color-lucky-point);
    color: var(--color-alabaster);
    
}

.bg-white{
    background-color: white;
}

.section-card{
    text-align: center;
    height: 100%;
    padding: 3rem 2.7rem;
    
    & i{
        color:var(--color-yellow-orange);
        font-size: 1.5rem;
    }

    & .section-card-title{
        transition: all .3s ease-in-out;
        &:hover{
            color: var(--color-yellow-orange);
        }
    }

    & .section-card-link a{
        color: var(--color-yellow-orange);
        text-decoration: none;
    }
}

</style>