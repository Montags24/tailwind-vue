<template>
  <main>
    <NavBar></NavBar>
    <section class="flex padding">
      <SideBar></SideBar>
    </section>
    <section class="xl:padding-l wide:padding-r padding-b">
      <Hero></Hero>
    </section>
    <section class="padding">
      <PopularProducts></PopularProducts>
    </section>
    <section class="padding">
      <SuperQuality></SuperQuality>
    </section>
    <section class="padding-x py-10">
      <Services></Services>
    </section>
    <section class="padding">
      <SpecialOffer></SpecialOffer>
    </section>
    <section class="bg-pale-blue padding">
      <CustomerReviews></CustomerReviews>
    </section>
    <section class="padding-x sm:py-32 py-16 w-full">
      <Subscribe></Subscribe>
    </section>
    <section class="bg-black padding-x padding-t pb-8 ">
      <FooterBar></FooterBar>
    </section>
  </main>
</template>

<script setup>
</script>

<script>
import NavBar from './components/NavBar.vue';
import CustomerReviews from './components/CustomerReviews.vue';
import FooterBar from './components/Footer.vue';
import Hero from './components/Hero.vue';
import PopularProducts from './components/PopularProducts.vue';
import Services from './components/Services.vue';
import SpecialOffer from './components/SpecialOffer.vue';
import SuperQuality from './components/SuperQuality.vue';
import Subscribe from './components/Subscribe.vue';
import SideBar from './components/SideBar.vue';

export default {
  components: {
    NavBar,
    CustomerReviews,
    FooterBar,
    Hero,
    PopularProducts,
    Services,
    SpecialOffer,
    SuperQuality,
    Subscribe,
    SideBar
  },
};

</script>

<style scoped></style>
