<template>
    <section id="products" class="max-container max-sm:mt-12">
        <div class="flex flex-col justify-start gap-5">
            <h2 class="text-4xl font-palanquin font-bold">Our <span class="text-coral-red">Popular</span> Products</h2>
            <p class="lg:max-w-lg mt-2 font-montserrat text-slate-gray">Experience top notch quality with our sought after
                products</p>
        </div>

        <div class="mt-16 grid grid-cols-1 lg:grid-cols-4 md:grid-cols-3 sm:grid-cols-2 gap-4">
            <PopularProductCard v-for="(product, index) in products" :key="index" :imgURL=product.imgURL
                :name="product.name" :price="product.price">
            </PopularProductCard>
        </div>

    </section>
</template>

<script>
import { products } from '../constants';
import PopularProductCard from '../components/PopularProductCard.vue'
export default {
    data() {
        return {
            products: products
        }
    },
    components: {
        PopularProductCard,
    },
}
</script>

<style lang="scss" scoped></style>