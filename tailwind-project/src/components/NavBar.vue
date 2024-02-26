<template>
    <header class="padding-x py-8 absolute z-10 w-full">
        <nav class="flex justify-between max-container">
            <a href="/">
                <img src="../assets/images/header-logo.svg" alt="header-logo" style="height: 29px;width: 130px;">
            </a>
            <ul class="flex flex-1 justify-center items-center gap-16 max-lg:hidden">
                <l1 v-for="(navlink, index) in navlinks" :key="index"><a href="{{ navlink.href }}"
                        class="font-montserrat leading-normal text-lg text-slate-gray">{{ navlink.label }}</a>
                </l1>
            </ul>
            <a href="/" class="font-montserrat leading-normal text-lg text-slate-gray hover:text-slate-800 hover:underline">
                Sign In/Explore
            </a>
        </nav>
    </header>
</template>

<script>
import hamburger from '../assets/icons/hamburger.svg'
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