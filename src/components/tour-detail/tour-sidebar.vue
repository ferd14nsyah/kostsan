<template>
    <div class="lg:col-span-4 md:col-span-5">
        <div class="p-4 rounded-md shadow dark:shadow-gray-700 sticky top-20">
            <div>
                <label class="font-semibold">Tanggal:</label>
                <div class="relative mt-2">
                    <VueDatePicker v-model="date" class="dp__theme_dark" :enable-time-picker="false"
                        placeholder="Select Your Date" text-input />
                </div>
            </div>

            <div class="mt-4">
                <div class="md:flex">
                    <div class="md:w-1/3">
                        <span class="font-medium">Dewasa:</span>
                    </div>

                    <div class="md:w-2/3 mt-4 md:mt-0">
                        <form>
                            <div class="form-icon relative">
                                <i data-feather="user" class="w-4 h-4 absolute top-3 start-4"></i>
                                <input type="number"
                                    class="w-full ps-12 py-2 px-3 h-10 bg-transparent dark:bg-slate-900 dark:text-slate-200 rounded outline-none border border-gray-100 dark:border-gray-800 focus:ring-0"
                                    placeholder="No. of person" id="Noperson" name="number" required="">
                            </div>
                        </form>
                    </div>
                </div>

                <div class="md:flex mt-4">
                    <div class="md:w-1/3">
                        <span class="font-medium">Anak:</span>
                    </div>

                    <div class="md:w-2/3 mt-4 md:mt-0">
                        <form>
                            <div class="form-icon relative">
                                <i data-feather="users" class="w-4 h-4 absolute top-3 start-4"></i>
                                <input type="number"
                                    class="w-full ps-12 py-2 px-3 h-10 bg-transparent dark:bg-slate-900 dark:text-slate-200 rounded outline-none border border-gray-100 dark:border-gray-800 focus:ring-0"
                                    placeholder="No. of children" id="Nochildren" name="number" required="">
                            </div>
                        </form>
                    </div>
                </div>
            </div>

            <div class="mt-4">
                <button
                    class="py-2 px-5 inline-block tracking-wide align-middle duration-500 text-base text-center bg-red-500 text-white rounded-md w-full">Cek</button>
            </div>

            <div class="mt-6">
                <h5 class="text-lg font-medium">Lokasi</h5>

                <div class="mt-3">
                    <iframe
                        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d39206.002432144705!2d-95.4973981212445!3d29.709510002925988!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x8640c16de81f3ca5%3A0xf43e0b60ae539ac9!2sGerald+D.+Hines+Waterwall+Park!5e0!3m2!1sen!2sin!4v1566305861440!5m2!1sen!2sin"
                        style="border:0" class="w-full h-[300px] rounded-full" allowfullscreen></iframe>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import VueDatePicker from '@vuepic/vue-datepicker';
import '@vuepic/vue-datepicker/dist/main.css'
export default {
    data() {
        return {

        }
    },
    components: {
        VueDatePicker
    }
}
</script>

<style lang="scss" scoped></style>