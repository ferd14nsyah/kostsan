<template>
    <div>
        <navbar :menuLight="'nav-light'" :navLight=true :searchMenu="'text-white'" />
        <!-- Start Hero -->
        <section
            class="relative table w-full py-36  bg-center bg-[url('../../assets/images/bg/cta.jpg')] bg-no-repeat bg-cover">
            <div class="absolute inset-0 bg-black opacity-80"></div>
            <div class="container relative">
                <div class="grid grid-cols-1 pb-8 text-center mt-10">
                    <h3 class="mb-6 text-4xl leading-normal tracking-wider font-semibold text-white">Hello ! <br> How
                        can we help you?</h3>

                    <div class="text-center subcribe-form mt-4 pt-2">
                        <form class="relative mx-auto max-w-xl">
                            <input type="text" id="help" name="name"
                                class="py-4 pe-40 ps-6 w-full h-[50px] outline-none text-black dark:text-white rounded-full bg-white opacity-70 dark:bg-slate-900 border border-gray-100 dark:border-gray-700"
                                placeholder="Search your questions or topic...">
                            <button type="submit"
                                class="py-2 px-5 inline-block font-semibold tracking-wide align-middle duration-500 text-base text-center absolute top-[2px] end-[3px] h-[46px] bg-red-500 text-white rounded-full">Search</button>
                        </form><!--end form-->
                    </div>
                </div><!--end grid-->
            </div><!--end container-->

            <div class="absolute text-center z-10 bottom-5 start-0 end-0 mx-3">
                <ul class="tracking-[0.5px] mb-0 inline-block">
                    <li
                        class="inline-block uppercase text-[13px] font-bold duration-500 ease-in-out text-white/50 hover:text-white">
                        <router-link to="/">TRAVOSY </router-link>
                    </li>
                    <li class="inline-block text-base text-white/50 mx-0.5 ltr:rotate-0 rtl:rotate-180"><i
                            class="mdi mdi-chevron-right"></i></li>
                    <li class="inline-block uppercase text-[13px] font-bold duration-500 ease-in-out text-white"
                        aria-current="page">Helpcenter</li>
                </ul>
            </div>
        </section><!--end section-->
        <!-- End Hero -->
        <helpcenter />
        <fooTer />
          <switcher :switcherBack=true />
    </div>
</template>

<script>
import navbar from '@/components/navbar.vue';
import helpcenter from '@/components/helpcenter/helpcenter.vue'
import fooTer from '@/components/footer.vue';
import switcher from '@/components/switcher.vue'
export default {
    name: "helpCenter",
    data() {
        return {

        }
    },
    components: {
        navbar,
        helpcenter,
        fooTer,
        switcher

    },
    mounted() {
        this.scrollToTop()
    },
    methods: {
        scrollToTop() {
            window.scrollTo(0, 0);
        }
    },
}
</script>

<style lang="scss" scoped></style>