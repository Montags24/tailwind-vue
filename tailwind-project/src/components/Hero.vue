<template>
    <div>
        <section id="home" class="w-full flex xl:flex-row flex-col justify-center min-h-screen gap-10 max-container">
            <div
                class="relative xl:w-2/5 flex flex-col justify-center items-start w-full max-xl:padding-x pt-28 border-coral-red border-2">
                <p>
                    Our Summer Collection
                </p>
                <h1>
                    <span>The New Arrival</span>
                    <br />
                    <span>Nike</span> Shoes
                </h1>
                <p>Discover stylish Nike arrivalsm quality comfort, and innovation for your active life.</p>
                <Button label="Shop Now" :iconURL=arrowRight></Button>

                <div class="flex justify-start items-start flex-wrap w-full mt-20 gap-16">
                    <div v-for="stat in statistics" :key="stat.label">
                        <p>{{ stat.value }}</p>
                        <p>{{ stat.label }}</p>
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
export default {
    components: {
        Button
    },
    data() {
        return {
            arrowRight: arrowRight,
            statistics: statistics
        }
    },
}
</script>

<style lang="scss" scoped></style>