<template>
    <navbar :menuLight="'nav-light'" :navLight=true :searchMenu="'text-white'" />
    <!-- Start Hero -->
    <section
        class="relative table w-full items-center py-36 bg-[url('../../assets/images/bg/cta.jpg')] bg-top bg-no-repeat bg-cover">
        <div class="absolute inset-0 bg-gradient-to-b from-slate-900/60 via-slate-900/80 to-slate-900"></div>
        <div class="container relative">
            <div class="grid grid-cols-1 pb-8 text-center mt-10">
                <h3 class="text-4xl leading-normal tracking-wider font-semibold text-white">Traveller Visiting Ice Cave
                    With Amazing Eye-catching Scenes</h3>

                <ul class="list-none mt-6">
                    <li class="inline-block text-white/50 mx-5"> <span class="text-white block">Author :</span> <span
                            class="block">Travosy</span></li>
                    <li class="inline-block text-white/50 mx-5"> <span class="text-white block">Date :</span> <span
                            class="block">8th February 2024</span></li>
                    <li class="inline-block text-white/50 mx-5"> <span class="text-white block">Time :</span> <span
                            class="block">8 Min Read</span></li>
                </ul>
            </div><!--end grid-->
        </div><!--end container-->

        <div class="absolute text-center z-10 bottom-5 start-0 end-0 mx-3">
            <ul class="tracking-[0.5px] mb-0 inline-block">
                <li
                    class="inline-block uppercase text-[13px] font-bold duration-500 ease-in-out text-white/50 hover:text-white">
                    <router-link to="/">Travosy</router-link>
                </li>
                <li class="inline-block text-base text-white/50 mx-0.5 ltr:rotate-0 rtl:rotate-180"><i
                        class="mdi mdi-chevron-right"></i></li>
                <li class="inline-block uppercase text-[13px] font-bold duration-500 ease-in-out text-white"
                    aria-current="page">Blog Detail</li>
            </ul>
        </div>
    </section><!--end section-->
    <!-- End Hero -->

    <!-- Start -->
    <section class="relative md:py-24 py-16">
        <div class="container">
            <div class="grid md:grid-cols-12 grid-cols-1 gap-6">
                <div class="lg:col-span-8 md:col-span-6">
                    <div class="relative overflow-hidden rounded-md shadow dark:shadow-gray-800">

                        <img src="../../../assets/images/blog/9.jpg" alt="">

                        <div class="p-6">
                            <p class="text-slate-400">The most well-known dummy text is the 'Lorem Ipsum', which is said
                                to have originated in the 16th century. Lorem Ipsum is composed in a pseudo-Latin
                                language which more or less corresponds to 'proper' Latin. It contains a series of real
                                Latin words. This ancient dummy text is also incomprehensible, but it imitates the
                                rhythm of most European languages in Latin script.</p>
                            <p
                                class="text-slate-400 italic border-x-4 border-red-500 rounded-ss-xl rounded-ee-xl mt-3 p-3">
                                " There are many variations of passages of Lorem Ipsum available, but the majority have
                                suffered alteration in some form, by injected humour, or randomised words which don't
                                look even slightly believable. "</p>
                            <p class="text-slate-400 mt-3">The advantage of its Latin origin and the relative
                                meaninglessness of Lorum Ipsum is that the text does not attract attention to itself or
                                distract the viewer's attention from the layout.</p>
                        </div>
                    </div>

                    <div class="p-6 rounded-md shadow dark:shadow-gray-800 mt-8">
                        <h5 class="text-lg font-semibold">Leave A Comment:</h5>

                        <form class="mt-8">
                            <div class="grid lg:grid-cols-12 lg:gap-6">
                                <div class="lg:col-span-6 mb-5">
                                    <div class="text-left">
                                        <label for="name" class="font-semibold">Your Name:</label>
                                        <input name="name" id="name" type="text"
                                            class="mt-3 w-full py-2 px-3 h-10 bg-transparent dark:bg-slate-900 dark:text-slate-200 rounded outline-none border border-gray-100 dark:border-gray-800 focus:ring-0"
                                            placeholder="Name :">
                                    </div>
                                </div>

                                <div class="lg:col-span-6 mb-5">
                                    <div class="text-left">
                                        <label for="email" class="font-semibold">Your Email:</label>
                                        <input name="email" id="email" type="email"
                                            class="mt-3 w-full py-2 px-3 h-10 bg-transparent dark:bg-slate-900 dark:text-slate-200 rounded outline-none border border-gray-100 dark:border-gray-800 focus:ring-0"
                                            placeholder="Email :">
                                    </div>
                                </div>
                            </div>

                            <div class="grid grid-cols-1">
                                <div class="mb-5">
                                    <div class="text-left">
                                        <label for="comments" class="font-semibold">Your Comment:</label>
                                        <textarea name="comments" id="comments"
                                            class="mt-3 w-full py-2 px-3 bg-transparent dark:bg-slate-900 dark:text-slate-200 rounded outline-none border border-gray-100 dark:border-gray-800 focus:ring-0 h-28"
                                            placeholder="Message :"></textarea>
                                    </div>
                                </div>
                            </div>
                            <button type="submit" id="submit" name="send"
                                class="py-2 px-5 inline-block tracking-wide align-middle duration-500 text-base text-center bg-red-500 text-white rounded-md w-full">Send
                                Message</button>
                        </form>
                    </div>
                </div>

                <div class="lg:col-span-4 md:col-span-6">
                    <div class="sticky top-20">
                        <h5
                            class="text-lg font-medium bg-gray-50 dark:bg-slate-800 shadow dark:shadow-gray-800 rounded-md p-2 text-center">
                            Author</h5>
                        <div class="text-center mt-8">
                            <img src="../../../assets/images/client/05.jpg"
                                class="h-20 w-20 mx-auto rounded-full shadow mb-4" alt="">

                            <a href=""
                                class="text-lg font-medium hover:text-red-500 transition-all duration-500 ease-in-out h5">Cristina
                                Romsey</a>
                            <p class="text-slate-400">Content Writer</p>
                        </div>

                        <h5
                            class="text-lg font-medium bg-gray-50 dark:bg-slate-800 shadow dark:shadow-gray-800 rounded-md p-2 text-center mt-8">
                            Social sites</h5>
                        <ul class="list-none text-center mt-8 space-x-0.5">
                            <li class="inline"><a href=""
                                    class="size-8 inline-flex items-center justify-center tracking-wide align-middle text-base border border-gray-100 dark:border-gray-800 rounded-md text-slate-400 hover:border-red-500 hover:text-white hover:bg-red-500"><i
                                        data-feather="facebook" class="size-4"></i></a></li>
                            <li class="inline"><a href=""
                                    class="size-8 inline-flex items-center justify-center tracking-wide align-middle text-base border border-gray-100 dark:border-gray-800 rounded-md text-slate-400 hover:border-red-500 hover:text-white hover:bg-red-500"><i
                                        data-feather="instagram" class="size-4"></i></a></li>
                            <li class="inline"><a href=""
                                    class="size-8 inline-flex items-center justify-center tracking-wide align-middle text-base border border-gray-100 dark:border-gray-800 rounded-md text-slate-400 hover:border-red-500 hover:text-white hover:bg-red-500"><i
                                        data-feather="twitter" class="size-4"></i></a></li>
                            <li class="inline"><a href=""
                                    class="size-8 inline-flex items-center justify-center tracking-wide align-middle text-base border border-gray-100 dark:border-gray-800 rounded-md text-slate-400 hover:border-red-500 hover:text-white hover:bg-red-500"><i
                                        data-feather="linkedin" class="size-4"></i></a></li>
                            <li class="inline"><a href=""
                                    class="size-8 inline-flex items-center justify-center tracking-wide align-middle text-base border border-gray-100 dark:border-gray-800 rounded-md text-slate-400 hover:border-red-500 hover:text-white hover:bg-red-500"><i
                                        data-feather="github" class="size-4"></i></a></li>
                            <li class="inline"><a href=""
                                    class="size-8 inline-flex items-center justify-center tracking-wide align-middle text-base border border-gray-100 dark:border-gray-800 rounded-md text-slate-400 hover:border-red-500 hover:text-white hover:bg-red-500"><i
                                        data-feather="youtube" class="size-4"></i></a></li>
                            <li class="inline"><a href=""
                                    class="size-8 inline-flex items-center justify-center tracking-wide align-middle text-base border border-gray-100 dark:border-gray-800 rounded-md text-slate-400 hover:border-red-500 hover:text-white hover:bg-red-500"><i
                                        data-feather="gitlab" class="size-4"></i></a></li>
                        </ul><!--end icon-->
                    </div>
                </div>
            </div>
        </div>

        <div class="container lg:mt-24 mt-16">
            <div class="grid grid-cols-1 mb-6 text-center">
                <h3 class="font-semibold text-3xl leading-normal">Related Blogs</h3>
            </div><!--end grid-->

            <div class="grid grid-cols-1 lg:grid-cols-3 md:grid-cols-2 gap-6 pt-6">
                <div v-for="item in blogs" :key="item" class="group relative overflow-hidden">
                    <div class="relative overflow-hidden rounded-md shadow dark:shadow-gray-800">
                        <img :src="item.image" class="group-hover:scale-110 group-hover:rotate-3 duration-500" alt="">

                    </div>

                    <div class="mt-6">
                        <div class="flex mb-4">
                            <span class="flex items-center text-slate-400 text-sm"><i data-feather="clock"
                                    class="size-4 text-slate-900 dark:text-white me-1.5"></i>5 min read</span>
                            <span class="text-slate-400 text-sm ms-3">by <a href=""
                                    class="text-slate-900 dark:text-white hover:text-red-500 dark:hover:text-red-500 font-medium">Travosy</a></span>
                        </div>

                        <router-link to="/blog-detail"
                            class="text-lg font-medium hover:text-red-500 duration-500 ease-in-out">{{ item.title
                            }}</router-link>
                        <p class="text-slate-400 mt-2">{{ item.desc }}</p>

                        <div class="mt-3">
                            <router-link to="/blog-detail" class="hover:text-red-500 inline-flex items-center">Read More
                                <i data-feather="chevron-right" class="size-4 ms-1"></i></router-link>
                        </div>
                    </div>
                </div><!--end content-->
            </div><!--end grid-->
        </div><!--end container-->
    </section><!--end section-->
    <!-- End -->
    <fooTer />
    <switcher :switcherBack=true />
</template>

<script>
import navbar from '@/components/navbar.vue'
import fooTer from '@/components/footer.vue';
import switcher from '@/components/switcher.vue'
export default {
    name: 'blogDetail',
    data() {
        return {

            blogs: [
                {
                    image: require('../../../assets/images/blog/6.jpg'),
                    title: 'Exploring the Timeless Allure of Fashion',
                    status: 'Dubai',
                    desc: 'This is required when, for example, the final text is not yet available.'
                },
                {
                    image: require('../../../assets/images/blog/7.jpg'),
                    title: 'A Chic Journey Through Fashion Trends',
                    status: 'Maldivas',
                    desc: 'This is required when, for example, the final text is not yet available.'
                },
                {
                    image: require('../../../assets/images/blog/8.jpg'),
                    title: 'Unique Autumn Fashion Ideas',
                    status: 'News',
                    desc: 'This is required when, for example, the final text is not yet available.'
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
        scrollToTop() {
            window.scrollTo(0, 0);
        }
    },
}
</script>

<style lang="scss" scoped></style>