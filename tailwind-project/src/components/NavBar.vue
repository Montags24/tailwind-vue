<template>
    <header class="padding-x py-8 absolute z-10 w-full shadow-lg">
        <nav class="flex justify-between max-container">
            <a href="/">
                <img src="../assets/images/header-logo.svg" alt="header-logo" style="height: 29px;width: 130px;">
            </a>
            <ul class="flex flex-1 justify-center items-center gap-16 max-lg:hidden">
                <l1 v-for="(navlink, index) in navlinks" :key="index"><a href="{{ navlink.href }}"
                        class="font-montserrat leading-normal text-lg text-slate-gray hover:underline">{{ navlink.label
                        }}</a>
                </l1>
            </ul>
            <a href="/"
                class="font-montserrat leading-normal text-lg text-slate-gray hover:text-slate-800 hover:underline max-lg:hidden">
                Sign In/Explore
            </a>
            <img src="../assets/icons/hamburger.svg" alt="hamburger" style="height: 25px;width: 25px;"
                class="hidden max-lg:block hover:cursor-pointer me-2">
        </nav>
    </header>
</template>

<script>
import { navLinks } from '../constants/index'
export default {
    data() {
        return {
            navlinks: navLinks
        }
    },


}
</script>

<style lang="scss" scoped></style>