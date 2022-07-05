<template>
    <div class="our-plans-card color-scorpion">
        <div class="our-plans-card-title pb-4">
            <h4 class="fw-bold">{{tariffPlan.type}}</h4>
        </div>
        <div class="our-plans-price pb-4 ">
            <span class="fs-1 position-relative">
                {{tariffPlan.price}}
                <div class="dollar-symbol">$</div>
                <div class="cents-symbol">99</div>
                <div class="label-monthly">monthly</div>
            </span>
            
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
        // salvo il singolo oggetto ricevuto dalla sezione
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

    & .our-plans-price{
        color: var(--color-science-blue);
        font-weight: 900;

        & .dollar-symbol{
            position: absolute;
            top: 5px;
            left: -10px;
            font-size: 1rem;
            color: var(--color-scorpion);
            font-weight: bold;
        }

        & .cents-symbol{
            position: absolute;
            top: 5px;
            right: -15px;
            font-size: .8rem;

        }

        & .label-monthly{
            position: absolute;
            bottom: 7px;
            right: -35px;
            font-size: .6rem;
            color: var(--color-scorpion);
        }
    }
}
</style>