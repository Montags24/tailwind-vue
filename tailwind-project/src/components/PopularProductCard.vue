<template>
    <div class="flex flex-col">
        <img :src="imgURL" :alt="name" style="width: 280px;height: 280px;">
        <div class="mt-8 flex justify-start gap-2.5">
            <img :src="star" alt="rating" style="width: 24px;height: 24px;">
            <p class="font-montserrat text-xl leading-normal text-slate-gray">(4.5)</p>
        </div>
        <h3 class="mt-2 text-2xl leading-normal font-semibold font-palanquin ">{{ name }}</h3>
        <p class="mt-2 font-semibold font-montserrat text-coral-red text-2xl leading-normal">{{ price }}</p>
    </div>
</template>

<script>
import { star } from '../assets/icons';
export default {
    props: {
        imgURL: {
            type: String
        },
        name: {
            type: String
        },
        price: {
            type: String
        },
    },
    data() {
        return {
            star: star
        }
    },

}
</script>

<style lang="scss" scoped></style>