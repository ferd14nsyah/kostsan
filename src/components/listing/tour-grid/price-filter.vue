<template>
    <div class="p-4 rounded-md shadow dark:shadow-gray-700 sticky top-20">
        <div>
            <h5 class="text-lg font-medium">Price Filter</h5>

            <div class="range-slider mt-3">
                <span class="flex justify-between pb-2">
                    <span>
                        <label for="" class="text-lg" >Rp</label>
                        <input type="number" class="text-slate-400 ps-1" value="500000" min="0" max="2000000"
                            v-model="numberValues[0]" @input="updateSliders" />
                    </span>

                    <span>
                        <label for="" class="text-lg">Rp</label>
                        <input type="number" class="text-slate-400 ps-1" value="12000000" min="0" max="200000000"
                            v-model="numberValues[1]" @input="updateSliders" />
                    </span>
                </span>
                <input value="500000" min="0" max="200000000" step="5" type="range" v-model="rangeValues[0]"
                    @input="updateNumbers" />
                <input value="12000000" min="0" max="200000000" step="5" type="range" v-model="rangeValues[1]"
                    @input="updateNumbers" />
            </div>
        </div>

        <div class="mt-6">
            <h5 class="text-lg font-medium">Reviews</h5>

            <div class="mt-3">
                <div class="flex items-center mb-0">
                    <input
                        class="form-checkbox rounded border-gray-100 dark:border-gray-800 text-red-500 focus:border-red-300 focus:ring focus:ring-offset-0 focus:ring-red-500/20 focus:ring-opacity-50 me-2"
                        type="checkbox" value="" id="5star">
                    <label class="form-checkbox-label text-slate-400" for="5star">
                        <ul class="font-medium list-none">
                            <li class="inline"><i class="mdi mdi-star text-amber-400 align-middle"></i></li>
                            <li class="inline"><i class="mdi mdi-star text-amber-400 align-middle"></i></li>
                            <li class="inline"><i class="mdi mdi-star text-amber-400 align-middle"></i></li>
                            <li class="inline"><i class="mdi mdi-star text-amber-400 align-middle"></i></li>
                            <li class="inline"><i class="mdi mdi-star text-amber-400 align-middle"></i></li>
                        </ul>
                    </label>
                </div>
                <div class="flex items-center mb-0">
                    <input
                        class="form-checkbox rounded border-gray-100 dark:border-gray-800 text-red-500 focus:border-red-300 focus:ring focus:ring-offset-0 focus:ring-red-500/20 focus:ring-opacity-50 me-2"
                        type="checkbox" value="" id="4star">
                    <label class="form-checkbox-label text-slate-400" for="4star">
                        <ul class="font-medium list-none">
                            <li class="inline"><i class="mdi mdi-star text-amber-400 align-middle"></i></li>
                            <li class="inline"><i class="mdi mdi-star text-amber-400 align-middle"></i></li>
                            <li class="inline"><i class="mdi mdi-star text-amber-400 align-middle"></i></li>
                            <li class="inline"><i class="mdi mdi-star text-amber-400 align-middle"></i></li>
                            <li class="inline"><i
                                    class="mdi mdi-star-outline text-slate-200 dark:text-gray-700 align-middle"></i>
                            </li>
                        </ul>
                    </label>
                </div>
                <div class="flex items-center mb-0">
                    <input
                        class="form-checkbox rounded border-gray-100 dark:border-gray-800 text-red-500 focus:border-red-300 focus:ring focus:ring-offset-0 focus:ring-red-500/20 focus:ring-opacity-50 me-2"
                        type="checkbox" value="" id="3star">
                    <label class="form-checkbox-label text-slate-400" for="3star">
                        <ul class="font-medium list-none">
                            <li class="inline"><i class="mdi mdi-star text-amber-400 align-middle"></i></li>
                            <li class="inline"><i class="mdi mdi-star text-amber-400 align-middle"></i></li>
                            <li class="inline"><i class="mdi mdi-star text-amber-400 align-middle"></i></li>
                            <li class="inline"><i
                                    class="mdi mdi-star-outline text-slate-200 dark:text-gray-700 align-middle"></i>
                            </li>
                            <li class="inline"><i
                                    class="mdi mdi-star-outline text-slate-200 dark:text-gray-700 align-middle"></i>
                            </li>
                        </ul>
                    </label>
                </div>
                <div class="flex items-center mb-0">
                    <input
                        class="form-checkbox rounded border-gray-100 dark:border-gray-800 text-red-500 focus:border-red-300 focus:ring focus:ring-offset-0 focus:ring-red-500/20 focus:ring-opacity-50 me-2"
                        type="checkbox" value="" id="2star">
                    <label class="form-checkbox-label text-slate-400" for="2star">
                        <ul class="font-medium list-none">
                            <li class="inline"><i class="mdi mdi-star text-amber-400 align-middle"></i></li>
                            <li class="inline"><i class="mdi mdi-star text-amber-400 align-middle"></i></li>
                            <li class="inline"><i
                                    class="mdi mdi-star-outline text-slate-200 dark:text-gray-700 align-middle"></i>
                            </li>
                            <li class="inline"><i
                                    class="mdi mdi-star-outline text-slate-200 dark:text-gray-700 align-middle"></i>
                            </li>
                            <li class="inline"><i
                                    class="mdi mdi-star-outline text-slate-200 dark:text-gray-700 align-middle"></i>
                            </li>
                        </ul>
                    </label>
                </div>
                <div class="flex items-center mb-0">
                    <input
                        class="form-checkbox rounded border-gray-100 dark:border-gray-800 text-red-500 focus:border-red-300 focus:ring focus:ring-offset-0 focus:ring-red-500/20 focus:ring-opacity-50 me-2"
                        type="checkbox" value="" id="1star">
                    <label class="form-checkbox-label text-slate-400" for="1star">
                        <ul class="font-medium list-none">
                            <li class="inline"><i class="mdi mdi-star text-amber-400 align-middle"></i></li>
                            <li class="inline"><i
                                    class="mdi mdi-star-outline text-slate-200 dark:text-gray-700 align-middle"></i>
                            </li>
                            <li class="inline"><i
                                    class="mdi mdi-star-outline text-slate-200 dark:text-gray-700 align-middle"></i>
                            </li>
                            <li class="inline"><i
                                    class="mdi mdi-star-outline text-slate-200 dark:text-gray-700 align-middle"></i>
                            </li>
                            <li class="inline"><i
                                    class="mdi mdi-star-outline text-slate-200 dark:text-gray-700 align-middle"></i>
                            </li>
                        </ul>
                    </label>
                </div>
            </div>
        </div>

        <div class="mt-6">
            <h5 class="text-lg font-medium">Booking Activity</h5>

            <div class="mt-3">
                <div class="flex items-center mb-0">
                    <input
                        class="form-checkbox rounded border-gray-100 dark:border-gray-800 text-red-500 focus:border-red-300 focus:ring focus:ring-offset-0 focus:ring-red-500/20 focus:ring-opacity-50 me-2"
                        type="checkbox" value="" id="Bali">
                    <label class="form-checkbox-label text-slate-400" for="Bali">Bali Park</label>
                </div>
                <div class="flex items-center mb-0">
                    <input
                        class="form-checkbox rounded border-gray-100 dark:border-gray-800 text-red-500 focus:border-red-300 focus:ring focus:ring-offset-0 focus:ring-red-500/20 focus:ring-opacity-50 me-2"
                        type="checkbox" value="" id="Paris">
                    <label class="form-checkbox-label text-slate-400" for="Paris">Paris</label>
                </div>
                <div class="flex items-center mb-0">
                    <input
                        class="form-checkbox rounded border-gray-100 dark:border-gray-800 text-red-500 focus:border-red-300 focus:ring focus:ring-offset-0 focus:ring-red-500/20 focus:ring-opacity-50 me-2"
                        type="checkbox" value="" id="Arcadia">
                    <label class="form-checkbox-label text-slate-400" for="Arcadia">Arcadia</label>
                </div>
                <div class="flex items-center mb-0">
                    <input
                        class="form-checkbox rounded border-gray-100 dark:border-gray-800 text-red-500 focus:border-red-300 focus:ring focus:ring-offset-0 focus:ring-red-500/20 focus:ring-opacity-50 me-2"
                        type="checkbox" value="" id="Culver">
                    <label class="form-checkbox-label text-slate-400" for="Culver">Culver City</label>
                </div>
                <div class="flex items-center mb-0">
                    <input
                        class="form-checkbox rounded border-gray-100 dark:border-gray-800 text-red-500 focus:border-red-300 focus:ring focus:ring-offset-0 focus:ring-red-500/20 focus:ring-opacity-50 me-2"
                        type="checkbox" value="" id="Long">
                    <label class="form-checkbox-label text-slate-400" for="Long">Long Beach</label>
                </div>
                <div class="flex items-center mb-0">
                    <input
                        class="form-checkbox rounded border-gray-100 dark:border-gray-800 text-red-500 focus:border-red-300 focus:ring focus:ring-offset-0 focus:ring-red-500/20 focus:ring-opacity-50 me-2"
                        type="checkbox" value="" id="California">
                    <label class="form-checkbox-label text-slate-400" for="California">California</label>
                </div>
            </div>
        </div>

        <div class="mt-6">
            <h5 class="text-lg font-medium">Tour Map</h5>

            <div class="mt-3">
                <iframe
                    src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d39206.002432144705!2d-95.4973981212445!3d29.709510002925988!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x8640c16de81f3ca5%3A0xf43e0b60ae539ac9!2sGerald+D.+Hines+Waterwall+Park!5e0!3m2!1sen!2sin!4v1566305861440!5m2!1sen!2sin"
                    style="border:0" class="w-full h-[300px] rounded-full" allowfullscreen></iframe>
            </div>
        </div>
    </div>

</template>

<script>
export default {
    name: 'priceFilter',
    data() {
        return {
            rangeValues: [50, 120],
            numberValues: [50, 120],
        }
    },
    methods: {
        updateNumbers() {
            const [slide1, slide2] = this.rangeValues;
            if (slide1 > slide2) {
                [this.numberValues[0], this.numberValues[1]] = [slide2, slide1];
            } else {
                this.numberValues = [slide1, slide2];
            }
        },
        updateSliders() {
            const [number1, number2] = this.numberValues;
            if (number1 > number2) {
                [this.rangeValues[0], this.rangeValues[1]] = [number2, number1];
            } else {
                this.rangeValues = [number1, number2];
            }
        },
    },
}
</script>

<style lang="scss" scoped></style>