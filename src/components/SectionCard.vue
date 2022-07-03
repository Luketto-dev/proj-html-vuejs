<template>
  <div class="section-card">
    <div><i class="fa-solid" :class="InfoCard.iconClass"></i></div>
    <div class="section-card-title">
        <h3 class="fw-bold pt-4">{{InfoCard.title}}</h3>
    </div>
    <div class="section-card-subtitle color-scorpion pt-3">
        {{InfoCard.subtitle}}
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
.section-card{
    background-color: white;
    text-align: center;
    height: 100%;
    padding: 3rem 2.5rem;
    
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
}

</style>