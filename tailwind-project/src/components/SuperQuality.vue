<template>
    <section id="about-us" class="flex justify-between items-center max-lg:flex-col gap-10 w-full max-container">
        <div class="flex flex-1 flex-col">
            <h2 class="font-palanquin text-4xl capitalize font-bold lg:mx-w-lg">
                We provide you
                <span class="text-coral-red">Super</span>
                <br />
                <span class="text-coral-red"> Quality</span> Shoes
            </h2>
            <p class="mt-4 lg:max-w-lg info-text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Reprehenderit,
                obcaecati! Exercitationem perferendis necessitatibus velit in impedit aperiam!</p>
            <p class="mt-4 lg:max-w-lg info-text">Lorem ipsum dolor sit aperiam id harum cumque ullam, non,
                maiores!</p>
            <div class="mt-11">
                <Button label="View Details"></Button>
            </div>
        </div>
        <div class="flex-1 flex justify-center items-center">
            <img :src="shoe8" alt="shoe8" style="width:570px;height:522px;">
        </div>

        <div class="border-2 border-coral-red p-20 ">

        </div>
    </section>
</template>

<script>
import Button from './Button.vue';
import { shoe8 } from '../assets/images';
export default {
    components: {
        Button,
    },
    data() {
        return {
            shoe8: shoe8
        }
    },
}
</script>

<style lang="scss" scoped></style>