<template>
    <form class="p-6 bg-white dark:bg-slate-900 rounded-xl shadow dark:shadow-gray-700">
        <div class="registration-form text-dark text-start">
            <div class="grid lg:grid-cols-5 md:grid-cols-2 grid-cols-1 gap-4">
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
                        <VueDatePicker v-model="date2" class="dp__theme_dark" :enable-time-picker="false"
                            placeholder="Select Your Date" text-input />
                    </div>
                </div>

                <div>
                    <label class="form-label font-medium text-slate-900 dark:text-white">No. of person:</label>
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

                <div class="lg:mt-[35px]">
                    <input type="submit" id="search-buy" name="search"
                        class="py-1 px-5 h-10 inline-block tracking-wide align-middle duration-500 text-base text-center bg-red-500 text-white rounded-md w-full cursor-pointer"
                        value="Search">
                </div>
            </div><!--end grid-->
        </div><!--end container-->
    </form><!--end form-->
</template>

<script>
import VueDatePicker from '@vuepic/vue-datepicker';
import '@vuepic/vue-datepicker/dist/main.css'

export default {
    name: 'selectedDate',
    data() {
        return {
            date: null,
            date2: null,
        }
    },
    components: {
        VueDatePicker

    }
}
</script>

<style lang="scss" scoped></style>