<template>
  <section class="banner position-relative">
    <div class="banner-text text-center">
        <div class="banner-title">
            <h2 class="fw-bold fs-1">Start Tour Free Consultation</h2>
        </div>
        <div class="banner-text-subtitle">
            <p class="fs-5 mb-3">Sed ut perspiciatis unde ominsistenatus error sit voluptatem accusantium doloremque laudantium</p> 
        </div>
        <div class="banner-text-button">
            <button class="btn my-btn-warning ">CONTACT US NOW</button>
        </div>
    </div>
    <div class="banner-overlay">

    </div>
  </section>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.banner{
    background-image: url("../../public/images/CTA-seo-1.jpg");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    opacity: 1;
    color: var(--color-alabaster);
    padding-top: 7.5rem;
    padding-bottom: 7.5rem ;

    & .banner-text{
        width: 30%;
        margin: 0 auto;
        position: relative;
        z-index: 10;
    }

    & .banner-overlay{
        position: absolute;
        top: 0;
        right: 0;
        left: 0;
        bottom: 0;
        background-color: black;
        opacity: .6;
    }
}
</style>