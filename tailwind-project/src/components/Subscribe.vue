<template>
    <section class="max-container flex justify-between items-center max-lg:flex-col gap-10" id="contact-us">
        <h3 class="text-4xl leading-[68px] lg:max-w-lg font-palanquin font-bold">Sign Up For
            <span class="text-coral-red">Updates</span> & Newsletters
        </h3>
        <div
            class="lg:max-x-[40%] w-full flex items-center max-sm:flex-col gap-5 p-2.5 sm:border sm:border-slate-gray rounded-full">
            <input type="text" placeholder="subscribe@nike.com" class="input bg-transparent">
            <div class="flex max-sm:justify-end items-center max-sm:w-full">
                <Button label="Sign Up" fullWidth></Button>
            </div>
        </div>
    </section>
</template>

<script>
import Button from './Button.vue';
export default {
    components: {
        Button,
    },
}
</script>

<style lang="scss" scoped></style>