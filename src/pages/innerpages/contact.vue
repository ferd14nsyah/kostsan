<template>
    <navbar />
    <!-- Google Map -->
    <div class="container-fluid relative mt-20">
        <div class="grid grid-cols-1">
            <div class="w-full leading-[0] border-0">
                <iframe
                    src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d39206.002432144705!2d-95.4973981212445!3d29.709510002925988!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x8640c16de81f3ca5%3A0xf43e0b60ae539ac9!2sGerald+D.+Hines+Waterwall+Park!5e0!3m2!1sen!2sin!4v1566305861440!5m2!1sen!2sin"
                    style="border:0" class="w-full h-[500px]" allowfullscreen></iframe>
            </div>
        </div><!--end grid-->
    </div><!--end container-->
    <!-- Google Map -->

    <!-- Start Section-->
    <section class="relative lg:py-24 py-16">
        <div class="container">
            <div class="grid md:grid-cols-12 grid-cols-1 items-center gap-6">
                <div class="lg:col-span-7 md:col-span-6">
                    <img src="../../assets/images/travel-train-station.svg" class="w-full max-w-[500px] mx-auto" alt="">
                </div>

                <div class="lg:col-span-5 md:col-span-6">
                    <div class="lg:ms-5">
                        <div class="bg-white dark:bg-slate-900 rounded-md shadow dark:shadow-gray-800 p-6">
                            <h3 class="mb-6 text-2xl leading-normal font-semibold">Get in touch !</h3>

                            <form>
                                <div class="grid lg:grid-cols-12 grid-cols-1 gap-3">
                                    <div class="lg:col-span-6">
                                        <label for="name" class="font-semibold">Your Name:</label>
                                        <input name="name" id="name" type="text"
                                            class="mt-2 w-full py-2 px-3 h-10 bg-transparent dark:bg-slate-900 dark:text-slate-200 rounded outline-none border border-gray-100 dark:border-gray-800 focus:ring-0"
                                            placeholder="Name :" required>
                                    </div>

                                    <div class="lg:col-span-6">
                                        <label for="email" class="font-semibold">Your Email:</label>
                                        <input name="email" id="email" type="email"
                                            class="mt-2 w-full py-2 px-3 h-10 bg-transparent dark:bg-slate-900 dark:text-slate-200 rounded outline-none border border-gray-100 dark:border-gray-800 focus:ring-0"
                                            placeholder="Email :" required>
                                    </div>

                                    <div class="lg:col-span-12">
                                        <label for="subject" class="font-semibold">Your Question:</label>
                                        <input name="subject" id="subject"
                                            class="mt-2 w-full py-2 px-3 h-10 bg-transparent dark:bg-slate-900 dark:text-slate-200 rounded outline-none border border-gray-100 dark:border-gray-800 focus:ring-0"
                                            placeholder="Subject :" required>
                                    </div>

                                    <div class="lg:col-span-12">
                                        <label for="comments" class="font-semibold">Your Comment:</label>
                                        <textarea name="comments" id="comments"
                                            class="mt-2 w-full py-2 px-3 h-28 bg-transparent dark:bg-slate-900 dark:text-slate-200 rounded outline-none border border-gray-100 dark:border-gray-800 focus:ring-0"
                                            placeholder="Message :"></textarea>
                                    </div>
                                </div>
                                <button type="submit" id="submit" name="send"
                                    class="py-2 px-5 inline-block tracking-wide align-middle duration-500 text-base text-center bg-red-500 text-white rounded-md mt-2">Send
                                    Message</button>
                            </form>
                        </div>
                    </div>
                </div>
            </div>
        </div><!--end container-->

        <div class="container lg:mt-24 mt-16">
            <div class="grid grid-cols-1 lg:grid-cols-3 md:grid-cols-2 gap-6">
                <div v-for="item in contacts" :key="item" class="text-center px-6">
                    <div class="relative text-transparent">
                        <div
                            class="size-20 bg-red-500/5 text-red-500 rounded-xl text-2xl flex align-middle justify-center items-center mx-auto shadow-sm dark:shadow-gray-800">
                            <i :data-feather="item.icon"></i>
                        </div>
                    </div>

                    <div class="content mt-7">
                        <h5 class="title h5 text-lg font-semibold">{{ item.name }}</h5>
                        <p class="text-slate-400 mt-3">{{ item.desc }}</p>

                        <div class="mt-5">
                            <a href="tel:+152534-468-854" v-if="item.status === '+152 534-468-854'"
                                class="text-red-500 font-medium">{{ item.status }}</a>
                            <a href="mailto:contact@example.com" v-if="item.status === 'contact@example.com'"
                                class="text-red-500 font-medium">{{ item.status }}</a>
                            <router-link to="" @click="toggle" v-if="item.status === 'View on Google map'"
                                data-type="iframe"
                                class="video-play-icon read-more lightbox text-red-500 font-medium">View on
                                Google map</router-link>
                        </div>
                    </div>
                </div>
            </div><!--end grid-->
        </div><!--end container-->
    </section><!--end section-->
    <!-- End Section-->
        <!-- iframe start  -->
        <div :class="isActive ? 'fixed' : 'hidden'" class="bg-black/[0.9] top-0 left-0 bottom-0 w-[100%] h-[100%] z-999">
        <div class="h-[100%] flex items-center justify-center">
            <iframe  src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d55431.05581015953!2d-95.461302!3d29.735948000000004!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x8640c36647a52ab1%3A0x70a301678672cb!2sBriargrove%20Park%2C%20Houston%2C%20TX%2C%20USA!5e0!3m2!1sen!2sin!4v1710322657489!5m2!1sen!2sin" width="700" height="500" frameborder="0"></iframe>
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
    <fooTer />
      <switcher :switcherBack=true />
</template>

<script>
import navbar from '@/components/navbar.vue'
import fooTer from '@/components/footer.vue';
import switcher from '@/components/switcher.vue'
export default {
    name: 'contactUs',
    data() {
        return {
            isActive: false,
            contacts: [
                {
                    icon: "phone",
                    name: "Phone",
                    desc: "The phrasal sequence of the is now so that many campaign and benefit",
                    status: "+152 534-468-854"
                },
                {
                    icon: "mail",
                    name: "Email",
                    desc: "The phrasal sequence of the is now so that many campaign and benefit",
                    status: "contact@example.com"
                },
                {
                    icon: "map-pin",
                    name: "Location",
                    desc: "C/54 Northwest Freeway, Suite 558, Houston, USA 485",
                    desc2: "",
                    status: "View on Google map"
                },
            ]
        }
    },
    components: {
        navbar,
        fooTer,
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
        }

    }
}
</script>

<style lang="scss" scoped></style>