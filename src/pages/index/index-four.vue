<template>
    <tagline />
    <navbar :menuLight="'nav-light'" :tagLine="'tagline-height'" :navLight=true :searchMenu="'text-white'" />
    <!-- Hero Start -->
    <section class="relative py-36  bg-cover jarallax"
        :style="{ backgroundImage: `url(${backgroundImagePath})`, backgroundPosition: 'center', backgroundAttachment: 'fixed' }"
        data-jarallax data-speed="0.5">
        <div class="absolute inset-0 bg-slate-900/40"></div>
        <div class="container relative">
            <div class="grid lg:grid-cols-12 md:grid-cols-2 mt-10 items-center gap-6">
                <div class="lg:col-span-7">
                    <h5 class="text-3xl font-dancing text-white">Find Your Ideal Stay</h5>
                    <h4 class="font-bold text-white lg:leading-normal leading-normal text-4xl lg:text-6xl mb-6 mt-5">
                        Where Do You <br> Want To Go?</h4>
                    <p class="text-white/70 text-xl max-w-xl">Planning for a trip? We will organize your trip with the
                        best places and within best budget!</p>

                    <div class="mt-6">
                        <a href=""
                            class="py-2 px-5 inline-block tracking-wide align-middle duration-500 text-base text-center bg-red-500 text-white rounded-md">View
                            Packages</a>
                        <a @click="toggle" data-type="youtube" data-id="S_CGed6E610"
                            class="size-10 cursor-pointer inline-flex items-center justify-center tracking-wide align-middle duration-500 text-base text-center rounded-full border border-red-500 bg-red-500 text-white ms-1 lightbox"><i
                                data-feather="video" class="h-4 w-4"></i></a><span
                            class="font-semibold ms-1 align-middle"></span>
                    </div>
                </div>

                <div class="lg:col-span-5">
                    <div
                        class="bg-white dark:bg-slate-900 rounded-xl shadow dark:shadow-gray-800 p-6 z-10 relative lg:ms-10">
                        <h4 class="mb-5 text-2xl font-semibold">Search Your Destinations</h4>

                        <form>
                            <div class="grid grid-cols-1 gap-3">
                                <div>
                                    <label class="form-label font-medium text-slate-900 dark:text-white">Search:</label>
                                    <div class="relative mt-2">
                                        <i data-feather="search" class="size-[18px] absolute top-[10px] start-3"></i>
                                        <input name="name" type="text" id="job-keyword"
                                            class="w-full py-2 px-3 ps-10 h-10 bg-transparent dark:bg-slate-900 dark:text-slate-200 rounded-md outline-none border border-gray-100 dark:border-gray-800 focus:ring-0"
                                            placeholder="Search">
                                    </div>
                                </div>

                                <div>
                                    <label class="form-label font-medium text-slate-900 dark:text-white">Select Your
                                        Date:</label>
                                    <div class="relative mt-2">
                                        <VueDatePicker v-model="date" class="dp__theme_dark" :enable-time-picker="false"
                                            placeholder="Select Your Date" text-input />

                                    </div>
                                </div>

                                <div>
                                    <label class="form-label font-medium text-slate-900 dark:text-white">Select Your
                                        Date:</label>
                                    <div class="relative mt-2">
                                        <VueDatePicker v-model="date2" class="dp__theme_dark"
                                            :enable-time-picker="false" placeholder="Select Your Date" text-input />

                                    </div>
                                </div>

                                <div>
                                    <label class="form-label font-medium text-slate-900 dark:text-white">No. of
                                        Person:</label>
                                    <div class="relative mt-2">
                                        <i data-feather="users" class="size-[18px] absolute top-[10px] start-3"></i>
                                        <select
                                            class="form-select w-full py-2 px-3 ps-10 h-10 bg-transparent dark:bg-slate-900 dark:text-slate-200 rounded-md outline-none border border-gray-100 dark:border-gray-800 focus:ring-0">
                                            <option disabled selected>No. of person</option>
                                            <option>1</option>
                                            <option>2</option>
                                            <option>3</option>
                                            <option>4</option>
                                            <option>5</option>
                                        </select>
                                    </div>
                                </div>

                                <div class="">
                                    <input type="submit" id="search-buy" name="search"
                                        class="py-1 px-5 h-10 inline-block tracking-wide align-middle duration-500 text-base text-center bg-red-500 text-white rounded-md w-full cursor-pointer"
                                        value="Search">
                                </div>
                            </div><!--end grid-->
                        </form>
                        <!-- end form -->
                    </div>
                </div>
            </div><!--end grid-->
        </div><!--end container-->
    </section><!--end section-->
    <div class="relative">
        <div class="absolute block w-full h-auto bottom-[25px] z-1 start-0">
            <a @click="scrollToBottom" class="cursor-pointer"><i
                    class="mdi mdi-arrow-down absolute top-0 start-0 end-0 text-center inline-flex items-center justify-center rounded-full bg-white dark:bg-slate-900 h-12 w-12 mx-auto shadow-md dark:shadow-gray-800"></i></a>
        </div>

        <div
            class="shape absolute sm:-bottom-px -bottom-[2px] start-0 end-0 overflow-hidden text-white dark:text-slate-900">
            <svg class="w-full h-auto scale-[2.0] origin-top" viewBox="0 0 2880 48" fill="none"
                xmlns="http://www.w3.org/2000/svg">
                <path d="M0 48H1437.5H2880V0H2160C1442.5 52 720 0 720 0H0V48Z" fill="currentColor"></path>
            </svg>
        </div>
    </div>
    <!-- Hero End -->
     <!-- iframe start  -->
     <div :class="isActive ? 'fixed' : 'hidden'" class="bg-black/[0.9] top-0 left-0 bottom-0 w-[100%] h-[100%] z-999">
        <div class="h-[100%] flex items-center justify-center">
            <iframe  src="https://www.youtube.com/embed/S_CGed6E610" width="700" height="500" frameborder="0"></iframe>
        </div><button class="text-slate-400 absolute top-[20px] right-[20px]">
            <svg stroke="currentColor" fill="none" stroke-width="2" viewBox="0 0 24 24" stroke-linecap="round"
                stroke-linejoin="round" class="size-5" height="1em" width="1em" xmlns="http://www.w3.org/2000/svg"
                @click="toggle">
                <line x1="18" y1="6" x2="6" y2="18"></line>
                <line x1="6" y1="6" x2="18" y2="18"></line>
            </svg>
        </button>
    </div>
     <!-- iframe end  -->
    <section class="relative md:py-24 py-16 overflow-hidden">
        <destinations :Destinations=false />
        <packages />
        <users />
        <askedquestions />
    </section>
    <fooTer />
    <switcher :switcherBack=true />
</template>

<script>
import tagline from '@/components/tagline.vue';
import navbar from '@/components/navbar.vue';
import destinations from '@/components/destinations/destinations-slider.vue';
import packages from '@/components/tour-packages/tour-packages-8item.vue';
import users from '@/components/users.vue'
import askedquestions from '@/components/asked-questions.vue';
import fooTer from '@/components/footer.vue';
import VueDatePicker from '@vuepic/vue-datepicker';
import '@vuepic/vue-datepicker/dist/main.css'
import backgroundImagePath from '../../assets/images/bg/6.jpg'
import switcher from '@/components/switcher.vue'
export default {
    name: 'indexFour',
    data() {
        return {
            isActive: false,
            date: null,
            date2: null,
            backgroundImagePath
        }
    },
    components: {
        tagline,
        navbar,
        destinations,
        packages,
        users,
        askedquestions,
        fooTer,
        VueDatePicker,
        switcher
    },
    mounted() {
        this.scrollToTop()
    },

    methods: {
        toggle() {
            if (!this.isActive) {
                this.isActive = true;
            } else {
                this.isActive = false;
            }
        },
        scrollToTop() {
            window.scrollTo(0, 0);
        },
        scrollToBottom() {
            window.scrollTo({ top: 700, behavior: "smooth" });
        }
    },
}
</script>

<style lang="scss" scoped></style>