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
                        <div class="p-6 rounded-md shadow dark:shadow-gray-800 bg-white dark:bg-slate-900">
                            <h5 class="text-lg font-semibold mb-4">Personal Detail :</h5>
                            <form>
                                <div class="grid lg:grid-cols-2 grid-cols-1 gap-5">
                                    <div v-for="item in details" :key="item">
                                        <label class="form-label font-medium">{{ item.name }}<span
                                                class="text-red-600">{{
                                        item.name2 }}</span></label>
                                        <div class="form-icon relative mt-2">
                                            <i :data-feather="item.icon" class="w-4 h-4 absolute top-3 start-4"></i>
                                            <input type="text"
                                                class="ps-12 w-full py-2 px-3 h-10 bg-transparent dark:bg-slate-900 dark:text-slate-200 rounded outline-none border border-gray-100 dark:border-gray-800 focus:ring-0"
                                                :placeholder="item.placeholder" id="firstname" name="name" required="">
                                        </div>
                                    </div>
                                </div><!--end grid-->

                                <div class="grid grid-cols-1">
                                    <div class="mt-5">
                                        <label class="form-label font-medium">Description : </label>
                                        <div class="form-icon relative mt-2">
                                            <i data-feather="message-circle" class="w-4 h-4 absolute top-3 start-4"></i>
                                            <textarea name="comments" id="comments"
                                                class="ps-11 w-full py-2 px-3 h-28 bg-transparent dark:bg-slate-900 dark:text-slate-200 rounded outline-none border border-gray-100 dark:border-gray-800 focus:ring-0"
                                                placeholder="Message :"></textarea>
                                        </div>
                                    </div>
                                </div><!--end row-->

                                <input type="submit" id="submit" name="send"
                                    class="py-2 px-5 inline-block font-semibold tracking-wide align-middle duration-500 text-base text-center bg-red-500 text-white rounded-md mt-5"
                                    value="Save Changes">
                            </form><!--end form-->
                        </div>

                        <div class="p-6 rounded-md shadow dark:shadow-gray-800 bg-white dark:bg-slate-900 mt-6">
                            <div class="grid lg:grid-cols-2 grid-cols-1 gap-5">
                                <div>
                                    <h5 class="text-lg font-semibold mb-4">Contact Info :</h5>

                                    <form>
                                        <div class="grid grid-cols-1 gap-5">
                                            <div v-for="item in details2" :key="item">
                                                <label class="form-label font-medium">{{ item.name }}</label>
                                                <div class="form-icon relative mt-2">
                                                    <i :data-feather="item.icon"
                                                        class="w-4 h-4 absolute top-3 start-4"></i>
                                                    <input name="number" id="number" type="number"
                                                        class="ps-12 w-full py-2 px-3 h-10 bg-transparent dark:bg-slate-900 dark:text-slate-200 rounded outline-none border border-gray-100 dark:border-gray-800 focus:ring-0"
                                                        :placeholder="item.placeholder">
                                                </div>
                                            </div>
                                        </div><!--end grid-->

                                        <button
                                            class="py-2 px-5 inline-block font-semibold tracking-wide align-middle duration-500 text-base text-center bg-red-500 text-white rounded-md mt-5">Add</button>
                                    </form>
                                </div><!--end col-->

                                <div>
                                    <h5 class="text-lg font-semibold mb-4">Change password :</h5>
                                    <form>
                                        <div class="grid grid-cols-1 gap-5">
                                            <div v-for="item in details3" :key="item">
                                                <label class="form-label font-medium">{{ item.name }}</label>
                                                <div class="form-icon relative mt-2">
                                                    <i :data-feather="item.icon"
                                                        class="w-4 h-4 absolute top-3 start-4"></i>
                                                    <input type="password"
                                                        class="ps-12 w-full py-2 px-3 h-10 bg-transparent dark:bg-slate-900 dark:text-slate-200 rounded outline-none border border-gray-100 dark:border-gray-800 focus:ring-0"
                                                        :placeholder="item.placeholder" required="">
                                                </div>
                                            </div>
                                        </div><!--end grid-->

                                        <button
                                            class="py-2 px-5 inline-block font-semibold tracking-wide align-middle duration-500 text-base text-center bg-red-500 text-white rounded-md mt-5">Save
                                            password</button>
                                    </form>
                                </div><!--end col-->

                            </div><!--end row-->
                        </div>

                        <div class="p-6 rounded-md shadow dark:shadow-gray-800 bg-white dark:bg-slate-900 mt-6">
                            <h5 class="text-lg font-semibold mb-5 text-red-600">Delete Account :</h5>

                            <p class="text-slate-400 mb-4">Do you want to delete the account? Please press below
                                "Delete" button</p>

                            <a href=""
                                class="py-2 px-5 inline-block font-semibold tracking-wide align-middle duration-500 text-base text-center bg-red-600 text-white rounded-md">Delete</a>
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
    name: "userSetting",
    data() {
        return {
            details: [
                {
                    name: 'First Name : ',
                    name2: '*',
                    icon: 'user',
                    placeholder: 'First Name:'
                },
                {
                    name: 'Last Name : ',
                    name2: '*',
                    icon: 'user-check',
                    placeholder: 'Last Name:'
                },
                {
                    name: 'Your Email : ',
                    name2: '*',
                    icon: 'mail',
                    placeholder: 'Email'
                },
                {
                    name: 'Occupation : ',
                    name2: '',
                    icon: 'bookmark',
                    placeholder: 'Occupation :'
                },
            ],
            details2: [
                {
                    name: 'Phone No. :',
                    icon: 'phone',
                    placeholder: 'Phone :'
                },
                {
                    name: 'Website :',
                    icon: 'globe',
                    placeholder: 'Url :'
                },
            ],
            details3: [
                {
                    name: 'Old password :',
                    icon: 'key',
                    placeholder: 'Old password'
                },
                {
                    name: 'New password :',
                    icon: 'key',
                    placeholder: 'New password'
                },
                {
                    name: 'Re-type New password :',
                    icon: 'key',
                    placeholder: 'Re-type New password'
                },
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