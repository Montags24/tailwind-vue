<template>
    <section class="flex justify-wrap items-center max-xl:flex-col-reverse gap-10 max-container">
        <div class="flex-1">
            <img :src="offer" alt="" style="width: 773px; height: 687px;" class="object-contain w-full">
        </div>
        <div class="flex flex-1 flex-col">
            <h2 class="font-palanquin text-4xl capitalize font-bold lg:mx-w-lg">
                <span class="text-coral-red">Special</span> Offer
            </h2>
            <p class="mt-4 lg:max-w-lg info-text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Reprehenderit,
                obcaecati! Exercitationem perferendis necessitatibus velit in impedit aperiam!</p>
            <p class="mt-4 lg:max-w-lg info-text">Lorem ipsum dolor sit aperiam id harum cumque ullam, non,
                maiores!</p>
            <div class="mt-11 flex flex-wrap gap-4">
                <Button label="View Details" :iconURL="arrowRight"></Button>
                <Button label="Learn More" backgroundColour="bg-white" borderColour="border-slate-gray"
                    textColour="text-slate-gray"></Button>
            </div>
        </div>
    </section>
</template>

<script>
import { offer } from '../assets/images';
import Button from './Button.vue';
import { arrowRight } from '../assets/icons';
export default {
    components: {
        Button,
    },
    data() {
        return {
            offer: offer,
            arrowRight: arrowRight
        }
    },

}
</script>

<style lang="scss" scoped></style>