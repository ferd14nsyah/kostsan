<template>
<section class="relative md:pt-48 md:pb-36 py-36 table w-full items-center bg-center" id="home" accordion
        :style="{ 'background-image': `url(${randomImage})` }">
        <div class="absolute inset-0 bg-slate-900/40"></div>
        <div class="container relative">
            <div class="grid grid-cols-1">
                <div class="text-center">
                    <h1 class="font-bold text-white lg:leading-normal leading-normal text-3xl lg:text-4xl mb-6 mt-5">Kahuripan Lestari Menjamin Kenyamanan Anda Tinggal</h1>
                    <div class="bg-black bg-transparent">
                        <p class="font-bold text-white/70 text-xl max-w-xl mx-auto">Mencari tempat tinggal untuk anak anda yang menempuh pendidikan? Atau mencari tempat penginapan selama perjalanan dinas? Atau anda ingin mendapatkan ruko bisnis yang nyaman dan strategis?</p>
                    </div>
                    

                    <div class="mt-6">
                        <SelectedTanggal />
                    </div>
                </div>
            </div><!--end grid-->
        </div><!--end container-->
    </section>

        <section class="relative md:py-24 py-16 overflow-hidden">
            <navbarkost/>
            <destinationskost/>
            <agencykost/>
            <Rentalkost/>
            <Rukokost/>
            <Userkostriview/>
            <Instapostkost/>
            </section>
            <Footerkost/>
               
</template>

<script>
import navbarkost from '@/components/navbarkost.vue';
import Image from '../../assets/images/bg/bg_1.jpg'
import Image2 from '../../assets/images/bg/bg_2.jpg'
import Image3 from '../../assets/images/bg/bg_3.jpg'
import Image4 from '../../assets/images/bg/bg_4.jpg'
import destinationskost from '@/components/destinations/Destinationkost.vue';
import agencykost from '@/components/Agencykost.vue';
import Rentalkost from '@/components/tour-packages/Rentalkost.vue';
import Rukokost from '../innerpages/listing/tour-grid/Rukokost.vue';
import Userkostriview from '@/components/Userkostriview.vue';
import Instapostkost from '@/components/Instapostkost.vue';
import Footerkost from '@/components/Footerkost.vue';


export default {
    name:"index-kost",
    data(){        
        return {
            randomImage: '',
            backgroundImages:[
                Image,
                Image2,
                Image3,
                Image4,
            ]
        }
    },
    mounted() {
        this.changeBackground();
        setInterval(this.changeBackground, 4000);
        this.scrollToTop()

    },
    components: {
        navbarkost,
        
        destinationskost,
        agencykost,
        Rentalkost,
        Rukokost,
        Userkostriview,
        Instapostkost,
        Footerkost,
    },
    methods: {
        changeBackground() {
            const randomIndex = Math.floor(Math.random() * this.backgroundImages.length);
            this.randomImage = this.backgroundImages[randomIndex];
        },
        scrollToTop() {
            window.scrollTo(0, 0);
        }
    },
    
}
</script>

<style lang="scss" scoped></style>