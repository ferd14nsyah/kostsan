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
                        <div class="rounded-md shadow dark:shadow-gray-800 bg-white dark:bg-slate-900">
                            <div class="p-6 border-b border-gray-100 dark:border-gray-700">
                                <h5 class="text-lg font-semibold">Account Notifications :</h5>
                            </div>

                            <div class="p-6">
                                <div class="flex justify-between pb-4">
                                    <h6 class="mb-0 font-medium">When someone mentions me</h6>
                                    <div class="">
                                        <input
                                            class="form-checkbox rounded border-gray-100 dark:border-gray-800 text-red-500 focus:border-red-300 focus:ring focus:ring-offset-0 focus:ring-red-200 focus:ring-opacity-50"
                                            type="checkbox" value="" id="noti1">
                                        <label class="form-check-label" for="noti1"></label>
                                    </div>
                                </div>
                                <div class="flex justify-between py-4 border-t border-gray-100 dark:border-gray-700">
                                    <h6 class="mb-0 font-medium">When someone follows me</h6>
                                    <div class="">
                                        <input
                                            class="form-checkbox rounded border-gray-100 dark:border-gray-800 text-red-500 focus:border-red-300 focus:ring focus:ring-offset-0 focus:ring-red-200 focus:ring-opacity-50"
                                            type="checkbox" value="" checked id="noti2">
                                        <label class="form-check-label" for="noti2"></label>
                                    </div>
                                </div>
                                <div class="flex justify-between py-4 border-t border-gray-100 dark:border-gray-700">
                                    <h6 class="mb-0 font-medium">When shares my activity</h6>
                                    <div class="">
                                        <input
                                            class="form-checkbox rounded border-gray-100 dark:border-gray-800 text-red-500 focus:border-red-300 focus:ring focus:ring-offset-0 focus:ring-red-200 focus:ring-opacity-50"
                                            type="checkbox" value="" id="noti3">
                                        <label class="form-check-label" for="noti3"></label>
                                    </div>
                                </div>
                                <div class="flex justify-between py-4 border-t border-gray-100 dark:border-gray-700">
                                    <h6 class="mb-0 font-medium">When someone messages me</h6>
                                    <div class="">
                                        <input
                                            class="form-checkbox rounded border-gray-100 dark:border-gray-800 text-red-500 focus:border-red-300 focus:ring focus:ring-offset-0 focus:ring-red-200 focus:ring-opacity-50"
                                            type="checkbox" value="" id="noti4">
                                        <label class="form-check-label" for="noti4"></label>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <div class="rounded-md shadow dark:shadow-gray-800 bg-white dark:bg-slate-900 mt-6">
                            <div class="p-6 border-b border-gray-100 dark:border-gray-700">
                                <h5 class="text-lg font-semibold">Marketing Notifications :</h5>
                            </div>

                            <div class="p-6">
                                <div class="flex justify-between pb-4">
                                    <h6 class="mb-0 font-medium">There is a sale or promotion</h6>
                                    <div class="">
                                        <input
                                            class="form-checkbox rounded border-gray-100 dark:border-gray-800 text-red-500 focus:border-red-300 focus:ring focus:ring-offset-0 focus:ring-red-200 focus:ring-opacity-50"
                                            type="checkbox" value="" id="noti5">
                                        <label class="form-check-label" for="noti5"></label>
                                    </div>
                                </div>
                                <div class="flex justify-between py-4 border-t border-gray-100 dark:border-gray-700">
                                    <h6 class="mb-0 font-medium">Company news</h6>
                                    <div class="">
                                        <input
                                            class="form-checkbox rounded border-gray-100 dark:border-gray-800 text-red-500 focus:border-red-300 focus:ring focus:ring-offset-0 focus:ring-red-200 focus:ring-opacity-50"
                                            type="checkbox" value="" id="noti6">
                                        <label class="form-check-label" for="noti6"></label>
                                    </div>
                                </div>
                                <div class="flex justify-between py-4 border-t border-gray-100 dark:border-gray-700">
                                    <h6 class="mb-0 font-medium">Weekly jobs</h6>
                                    <div class="">
                                        <input
                                            class="form-checkbox rounded border-gray-100 dark:border-gray-800 text-red-500 focus:border-red-300 focus:ring focus:ring-offset-0 focus:ring-red-200 focus:ring-opacity-50"
                                            type="checkbox" value="" checked id="noti7">
                                        <label class="form-check-label" for="noti7"></label>
                                    </div>
                                </div>
                                <div class="flex justify-between py-4 border-t border-gray-100 dark:border-gray-700">
                                    <h6 class="mb-0 font-medium">Unsubscribe News</h6>
                                    <div class="">
                                        <input
                                            class="form-checkbox rounded border-gray-100 dark:border-gray-800 text-red-500 focus:border-red-300 focus:ring focus:ring-offset-0 focus:ring-red-200 focus:ring-opacity-50"
                                            type="checkbox" value="" checked id="noti8">
                                        <label class="form-check-label" for="noti8"></label>
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
    name: "userNotification",
    data() {
        return {

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