<template>
    <section class="max-container">
        <h3 class="font-palanquin text-center text-4xl font-bold">What Our
            <span class="text-coral-red">Customers</span>
            Say?
        </h3>
        <p class="info-text m-auto mt-4 max-w-lg text-center">Hear genuine stories from our satisfied customers about their
            exceptional experiences with us</p>
        <div class="mt-20 flex flex-1 justify-evenly items-center max-lg:flex-col gap-14">
            <CustomerReviewCard v-for="(review, index) in reviews" :key="index" :imgURL="review.imgURL"
                :customerName="review.customerName" :rating="review.rating" :feedback="review.feedback">
            </CustomerReviewCard>
        </div>
    </section>
</template>

<script>
import CustomerReviewCard from '../components/CustomerReviewCard.vue'
import { reviews } from '../constants'
export default {
    components: {
        CustomerReviewCard,
    },
    data() {
        return {
            reviews: reviews
        }
    },
}
</script>

<style lang="scss" scoped></style>