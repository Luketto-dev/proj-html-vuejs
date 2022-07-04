<template>
  <div class="section-card" :class="InfoCard.linkText ? 'bg-lucky-point' : 'bg-white'">
    <div><i class="fa-solid" :class="InfoCard.iconClass"></i></div>
    <div class="section-card-title">
        <h3 class="fw-bold pt-4">{{InfoCard.title}}</h3>
    </div>
    <div class="section-card-subtitle pt-3" :class="InfoCard.linkText ? 'color-alabaster' : 'color-scorpion'">
        {{InfoCard.subtitle}}
    </div>
    <div v-if="InfoCard.linkText" class="section-card-link pt-4">
        <a href="">{{InfoCard.linkText}}</a>
    </div>
  </div>
</template>

<script>
export default {
    props:{
        InfoCard : Object
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