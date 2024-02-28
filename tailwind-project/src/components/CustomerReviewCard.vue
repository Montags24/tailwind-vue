<template>
    <section class="flex flex-col items-center justify-center text-center">
        <img :src="imgURL" alt="profile photo" style="width: 100px; height: 100px;" class="rounded-full object-cover">
        <p class="text-lg mt-10 max-w-lg sm:max-w-md info-text">{{ feedback }}</p>
        <div class="max-lg:mt-6 mt-8 flex justify-start gap-2.5">
            <img :src="star" alt="rating" style="width: 24px;height: 24px;">
            <p class="font-montserrat text-xl leading-normal text-slate-gray">({{ rating }})</p>
        </div>
        <p class="text-3xl font-palanquin font-semibold leading-normal">{{ customerName }}</p>

    </section>
</template>

<script>
import { star } from '../assets/icons';
export default {
    props: {
        imgURL: {
            type: String,
        },
        customerName: {
            type: String,
        },
        rating: {
            type: Number,
        },
        feedback: {
            type: String,
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