<template>
    <div>
        <navbar />
        <!-- Start Hero -->
        <section class="relative lg:pb-24 pb-16 md:mt-[84px] mt-[70px]">
            <div class="md:container container-fluid relative">
                <div
                    class="relative overflow-hidden md:rounded-md shadow dark:shadow-gray-800 h-52 bg-[url('../../assets/images/bg/bg_kos.jpg')] bg-center bg-no-repeat bg-cover">
                </div>
            </div><!--end container-->

            <div class="container relative md:mt-24 mt-16">
                <div class="md:flex">
                    <div class="lg:w-1/4 md:w-1/3 md:px-3">
                        <usertab />
                    </div>

                    <div class="lg:w-3/4 md:w-2/3 md:px-3 mt-6 md:mt-0">
                        <div class="rounded-md shadow dark:shadow-gray-800 bg-white dark:bg-slate-900 mt-6">
                            <div class="p-6 border-b border-gray-100 dark:border-gray-700">
                                <h5 class="text-lg font-semibold">Social Profiles :</h5>
                            </div>

                            <div class="p-6">
                                <div class="md:flex ">
                                    <div class="md:w-1/3">
                                        <span class="font-medium">Twitter</span>
                                    </div>

                                    <div class="md:w-2/3 mt-4 md:mt-0">
                                        <form>
                                            <div class="form-icon relative">
                                                <i data-feather="twitter" class="w-4 h-4 absolute top-3 start-4"></i>
                                                <input type="text"
                                                    class="ps-12 w-full py-2 px-3 h-10 bg-transparent dark:bg-slate-900 dark:text-slate-200 rounded outline-none border border-gray-100 dark:border-gray-800 focus:ring-0"
                                                    placeholder="Twitter Profile Name" id="twitter_name" name="name"
                                                    required="">
                                            </div>
                                        </form>

                                        <p class="text-slate-400 mt-1">Add your Twitter username (e.g. jesus).</p>
                                    </div>
                                </div>
                                <div v-for="item in socials" :key="item" class="md:flex mt-8">
                                    <div class="md:w-1/3">
                                        <span class="font-medium">{{ item.name }}</span>
                                    </div>

                                    <div class="md:w-2/3 mt-4 md:mt-0">
                                        <form>
                                            <div class="form-icon relative">
                                                <i :data-feather="item.icon" class="w-4 h-4 absolute top-3 start-4"></i>
                                                <input type="text"
                                                    class="ps-12 w-full py-2 px-3 h-10 bg-transparent dark:bg-slate-900 dark:text-slate-200 rounded outline-none border border-gray-100 dark:border-gray-800 focus:ring-0"
                                                    :placeholder="item.placeholder" id="twitter_name" name="name"
                                                    required="">
                                            </div>
                                        </form>

                                        <p class="text-slate-400 mt-1">{{ item.desc }}</p>
                                    </div>
                                </div>
                                <div class="md:flex">
                                    <div class="md:w-1/3">
                                        <span class="font-medium"></span>
                                        <button
                                            class="py-2 px-5 inline-block font-semibold tracking-wide align-middle duration-500 text-base text-center bg-red-500 text-white rounded-md mt-5">Save
                                            Social Profile</button>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div><!--end grid-->
            </div><!--end container-->
        </section><!--end section-->
        <!-- End Hero -->

    </div>
    <fooTer />
  <switcher :switcherBack=true />
</template>

<script>
import navbar from '@/components/NavbarGwh.vue';
import usertab from '@/components/account-tab.vue'
import fooTer from '@/components/FooterGwh.vue';
import switcher from '@/components/switcher.vue'
export default {
    name: "userSocial",
    data() {
        return {
            socials: [
                {
                    name: "Facebook",
                    icon: "facebook",
                    placeholder: "Facebook Profile Name",
                    desc: "Add your Facebook username (e.g. jesus)."
                },
                {
                    name: "Instagram",
                    icon: "instagram",
                    placeholder: "Instagram Profile Name",
                    desc: "Add your Instagram username (e.g. jesus)."
                },
                {
                    name: "Linkedin",
                    icon: "linkedin",
                    placeholder: "Linkedin Profile Name",
                    desc: "Add your Linkedin username."
                },
                {
                    name: "Youtube",
                    icon: "youtube",
                    placeholder: "Youtube url",
                    desc: "Add your Youtube url."
                }
            ]
        }
    },
    components: {
        navbar,
        usertab,
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