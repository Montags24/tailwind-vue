<template>
    <div>
        <section id="home" class="w-full flex xl:flex-row flex-col justify-center min-h-screen gap-10 max-container">
            <div class="relative xl:w-2/5 flex flex-col justify-center items-start w-full max-xl:padding-x pt-28 ">
                <p class="text-xl font-montserrat text-coral-red">
                    Our Summer Collection
                </p>
                <h1 class="mt-10 font-palanquin text-8xl max-sm:text-[72px] max-sm:leading-[82px] font-bold">
                    <span class="xl:bg-white xl:whitespace-nowrap relative z-10 pr-10">The New Arrival</span>
                    <br />
                    <span class="text-coral-red inline-block mt-3">Nike</span> Shoes
                </h1>
                <p class="font-montserrat text-slate-gray text-lg leading-8 mt-6 mb-14 sm:max-w-sm">Discover stylish Nike
                    arrivalsm quality comfort, and innovation
                    for your active
                    life.</p>
                <Button label="Shop Now" :iconURL=arrowRight></Button>

                <div class="flex justify-start items-start flex-wrap w-full mt-20 gap-16">
                    <div v-for="stat in statistics" :key="stat.label">
                        <p class="text-4xl font-palanquin font-bold">{{ stat.value }}</p>
                        <p class="leading-7 font-montserrat text-slate-gray">{{ stat.label }}</p>
                    </div>
                </div>
            </div>

            <div
                class="relative flex-1 flex justify-center items-center xl:min-h-screen max-xl:py-40 bg-primary bg-hero bg-cover bg-center">
                <img :src="bigShoe1" alt="big shoe" style="width: 610px;height: 500px" class="object-contain relative z-10">
                <div class="flex sm:gap-6 gap-4 absolute -bottom-[5%] sm:left-[10%] max-sm:px-6">
                    <div v-for="shoe in shoes" :key="shoe">
                        <ShoeCard :imgURL=shoe :bigShoeImage=bigShoe1 @emitShoeImage="changeBigShoeImage"></ShoeCard>
                    </div>
                </div>
            </div>
        </section>
    </div>
</template>

<script>
import Button from './Button.vue';
import { arrowRight } from '../assets/icons';
import { statistics } from '../constants';
import { bigShoe1 } from '../assets/images';
import { shoes } from '../constants';
import ShoeCard from '../components/ShoeCard.vue'
export default {
    components: {
        Button,
        ShoeCard
    },
    data() {
        return {
            arrowRight: arrowRight,
            statistics: statistics,
            bigShoe1: bigShoe1,
            shoes: shoes
        }
    },
    methods: {
        changeBigShoeImage(shoeImg) {
            this.bigShoe1 = shoeImg
        }
    },
}
</script>

<style lang="scss" scoped></style>
<style lang="scss" scoped></style>