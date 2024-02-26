<template>
    <button
        class="flex justify-center items-center gap-2 px-7 py-3 border font-montserrat text-lg leading-none bg-coral-red rounded-full text-white border-coral-red">{{
            label
        }} <img :src="iconURL" alt="arrow right" class="ml-2 rounded-full w-5 h-5"></button>
</template>

<script>
export default {
    props: {
        label: {
            type: String,
            default: "Click Me"
        },
        iconURL: {
            type: String,
            default: ""
        }
    },
}
</script>

<style lang="scss" scoped></style>