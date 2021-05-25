<template>
    <div class="relative h-36 md:h-48 mb-12">
        <div
            class="absolute inset-0 flex items-center justify-center bg-gradient-to-b from-yellow-200 via-yellow-300 to-yellow-400"
        >
            <div class="mx-auto grid grid-cols-1 gap-4 align-center">
                <p class="text-center block">
                    Reserve now to get 10% off your first order
                </p>
                <button
                    class="rounded-lg text-xs md:text-base uppercase bg-blue-500 hover:bg-blue-700 text-white font-bold p-4"
                >
                    Make a reservation
                </button>
            </div>
        </div>
    </div>

    <!-- <div
        class="container mx-auto grid grid-cols-1 md:grid-cols-2 gap-4 place-items-center"
    >
        <div
            class="h-48 bg-gradient-to-l from-pink-500 via-red-500 to-yellow-500"
        >
            <div
                class="flex flex-wrap content-around justify-center gap-2 md:gap-4"
            >
                <button
                    class="text-xs md:text-base bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-2 rounded"
                >
                    Make a reservation
                </button>
                <button
                    class="text-xs md:text-base bg-white hover:bg-gray-200 text-gray-700 font-bold py-2 px-2 rounded"
                >
                    <a href="/menu" @click="handleSliderButton('/menu')"
                        >View Menu</a
                    >
                </button>
            </div>
        </div> -->
</template>


<script>
export default {
    name: "Cta",
    components: {},
    data() {
        return {};
    },
    mounted() {},
    methods: {},
    computed: {},
};
</script>



