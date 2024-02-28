<template>
    <button
        class="flex justify-center items-center gap-2 px-7 py-3 border font-montserrat text-lg leading-none rounded-full"
        :class="[backgroundColour ? [backgroundColour, borderColour, textColour] : ['text-white', 'bg-coral-red'], fullWidth ? 'w-full' : '']">
        {{ label }}
        <img v-if="iconURL" :src="iconURL" alt="arrow right" class="ml-2 rounded-full w-5 h-5">
    </button>
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
        },
        backgroundColour: {
            type: String,
            default: null
        },
        borderColour: {
            type: String,
            default: null
        },
        textColour: {
            type: String,
            default: null
        },
        fullWidth: {
            type: String,
            default: null
        }
    },
}
</script>

<style lang="scss" scoped></style>