<template>
  <section class="banner">
    <div class="banner-text text-center">
        <div class="banner-title">
            <h2 class="fw-bold">Start Tour Free Consultation</h2>
        </div>
        <div class="banner-text-subtitle">
            <p>Sed ut perspiciatis unde ominsistenatus error sit voluptatem accusantium doloremque laudantium</p> 
        </div>
        <div class="banner-text-button">
            <button class="btn my-btn-warning">CONTACT US NOW</button>
        </div>
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
    opacity: .9;
    color: var(--color-alabaster);
    padding-top: 6rem;
    padding-bottom: 6rem ;

    & .banner-text{
        width: 25%;
        margin: 0 auto;
    }
}
</style>