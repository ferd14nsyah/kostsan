<template>
    <div>
<!-- Start Terms & Conditions -->
<section class="relative md:py-24 py-16">
            <div class="container relative">
                <div class="md:flex justify-center">
                    <div class="md:w-3/4">
                        <div class="p-6 bg-white dark:bg-slate-900 shadow dark:shadow-gray-800 rounded-md">
                            <h5 class="text-xl font-semibold mb-4">Overview :</h5>
                            <p class="text-slate-400">It seems that only fragments of the original text remain in the Lorem Ipsum texts used today. One may speculate that over the course of time certain letters were added or deleted at various positions within the text.</p>
                            <p class="text-slate-400">In the 1960s, the text suddenly became known beyond the professional circle of typesetters and layout designers when it was used for Letraset sheets (adhesive letters on transparent film, popular until the 1980s) Versions of the text were subsequently included in DTP programmes such as PageMaker etc.</p>
                            <p class="text-slate-400">There is now an abundance of readable dummy texts. These are usually used when a text is required purely to fill a space. These alternatives to the classic Lorem Ipsum texts are often amusing and tell short, funny or nonsensical stories.</p>
                        
                            <h5 class="text-xl font-semibold mb-4 mt-8">We use your information to :</h5>
                            <ul class="list-none text-slate-400 mt-4">
                                <li v-for="item in privacys" :key="item" class="flex ms-0 mt-2"><i class="mdi mdi-chevron-right text-red-500 text-lg align-middle me-2"></i>{{item.name}}</li>
                            </ul>

                            <h5 class="text-xl font-semibold mb-4 mt-8">Information Provided Voluntarily :</h5>
                            <p class="text-slate-400">In the 1960s, the text suddenly became known beyond the professional circle of typesetters and layout designers when it was used for Letraset sheets (adhesive letters on transparent film, popular until the 1980s) Versions of the text were subsequently included in DTP programmes such as PageMaker etc.</p>

                            <div class="mt-8">
                                <a href="" class="py-2 px-5 inline-block font-semibold tracking-wide border align-middle duration-500 text-base text-center bg-red-500 hover:bg-red-600 border-red-500 hover:border-red-600 text-white rounded-md">Print</a>
                            </div>
                        </div>
                    </div><!--end -->
                </div><!--end grid-->
            </div><!--end container-->
        </section><!--end section-->
        <!-- End Terms & Conditions -->
    </div>
</template>

<script>
    export default {
        name: "privacyPage",
        data() {
            return {
                privacys:[
                    {
                        name: "Digital Marketing Solutions for Tomorrow"
                    },
                    {
                        name: "Our Talented & Experienced Marketing Agency"
                    },
                    {
                        name: "Create your own skin to match your brand"
                    },
                    {
                        name: "Digital Marketing Solutions for Tomorrow"
                    },
                    {
                        name: "Our Talented & Experienced Marketing Agency"
                    },
                    {
                        name: "Create your own skin to match your brand"
                    },
                ]
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>