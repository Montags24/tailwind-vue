<template>
    <section id="services" class="max-container flex flex-wrap justify-center gap-9">
        <ServicesCard v-for="service in services" :key="service.label" :imgURL="service.imgURL" :label="service.label"
            :subtext="service.subtext"></ServicesCard>
    </section>
</template>

<script>
import { services } from '../constants';
import ServicesCard from './ServicesCard.vue';

export default {
    components: {
        ServicesCard,
    },
    data() {
        return {
            services: services
        }
    },

}
</script>

<style lang="scss" scoped></style>