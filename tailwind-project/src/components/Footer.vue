<template>
    <footer class="max-container">
        <div class="flex justify-between items-start gap-20 flex-wrap max-lg:flex-col">
            <div class="flex flex-col items-start">
                <a href="/">
                    <img :src="footerLogo" alt="nike logo" style="width: 150px;height: 46px;">
                </a>
                <p class="mt-6 text-base leading-7 font-montserrat text-white-400 sm:max-w-sm">Get shoes ready for the new
                    term at your nearest Nike store. Find your
                    perfect size in store. Get Rewards</p>

                <div class="flex items-center gap-5 mt-8">
                    <div v-for="(media, index) in socialMedia" :key="index">
                        <div class="flex justify-center items-center w-12 h-12 bg-white rounded-full">
                            <img :src="media.src" :alt="media.alt" style="width: 24px; height: 24px;">
                        </div>
                    </div>
                </div>

            </div>
            <div class="flex flex-1 justify-between lg:gap-10 gap-20 flex-wrap">
                <div v-for="footerLink in footerLinks" :key="footerLink.title">
                    <h4 class="text-white text-2xl font-montserrat mb-6">{{ footerLink.title }}</h4>
                    <ul v-for="(link, index) in footerLink.links" :key="index">
                        <li class="mt-1"><a :href="link.link" class="text-slate-gray hover:text-white-400">{{ link.name
                        }}</a></li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
import { footerLogo } from '../assets/images';
import { socialMedia } from '../constants';
import { footerLinks } from '../constants';
export default {
    data() {
        return {
            footerLogo: footerLogo,
            socialMedia: socialMedia,
            footerLinks: footerLinks
        }
    },
}
</script>

<style lang="scss" scoped></style>