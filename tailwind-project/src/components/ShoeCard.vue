<template>
    <div class="gap-2 hover:cursor-pointer max-sm:flex-1">
        <div class="flex justify-center items-center bg-card bg-center bg-cover sm:w-40 sm:h-40 rounded-xl p-4 border-2"
            :class="(bigShoeImage == imgURL.bigShoe) ? 'border-coral-red ' : 'border-transparent'"
            @click="emitShoeImage(imgURL)">
            <img :src="imgURL.thumbnail" alt="shoe image" style="width: 120px; height: 103px">
        </div>
    </div>
</template>

<script>
export default {
    emits: ['emitShoeImage'],
    props: {
        imgURL: {
            type: Object
        },
        bigShoeImage: { String }
    },
    methods: {
        emitShoeImage(imgURL) {
            this.$emit('emitShoeImage', imgURL.bigShoe)
        }
    }
}
</script>


<style lang="scss" scoped></style>