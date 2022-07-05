<template>
    <div class="our-plans-card color-scorpion">
        <div class="our-plans-card-title pb-4">
            <h4 class="fw-bold">{{tariffPlan.type}}</h4>
        </div>
        <div class="our-plans-price pb-4 ">
            <div class="fs-1">{{tariffPlan.price}}</div>
        </div>
        <div class="our-plans-project pb-4">
            {{tariffPlan.pojects}}
        </div>
        <div class="our-plans-storage pb-4">
            {{tariffPlan.storage}}
        </div>
        <div class="our-plans-users pb-4">
            {{tariffPlan.users}}
        </div>
        <button class="btn my-btn-outline">START TODAY</button>
    </div>
</template>

<script>
export default {
    props:{
        tariffPlan: Object
    }

}
</script>

<style lang="scss" scoped>
.our-plans-card{
    background-color: var(--color-alabaster);
    text-align: center;
    padding-top: 2rem;
    padding-bottom: 2rem;
}
</style>