<template>
    <div class="picture-card">
        <img :src="'../../public/images/' + InfoCard" alt="">
    </div>
</template>

<script>
export default {
    props:{
        InfoCard: String
    }

}
</script>

<style lang="scss" scoped>

</style>