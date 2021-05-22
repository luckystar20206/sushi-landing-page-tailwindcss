
<template>
    <div class="relative h-screen mb-12">
        <div
            class="absolute bg-cover bg-no-repeat inset-0 flex items-center justify-center"
            style="
                background-image: url('/images/bg-home2.jpg');
                background-position: 0 -200px;
            "
        >
            <div class="">
                <div
                    class="text-1xl sm:text-4xl bg-black bg-opacity-50 text-white text-center block px-8 py-2 -mt-16 md:py-8"
                >
                    <span class="opacity-100">{{ headline }}</span>
                </div>
                <div
                    class="h-32 flex flex-wrap content-around justify-center gap-4"
                >
                    <button
                        class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded"
                    >
                        Make a reservation
                    </button>
                    <button
                        class="bg-white hover:bg-gray-200 text-gray-700 font-bold py-2 px-4 rounded"
                    >
                        <a href="menu">View Menu</a>
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>


<script>
export default {
    name: "HomeBackground",
    components: {},
    data() {
        return {
            headline:
                "Enjoy fresh fish & drinks. Immerse yourself in true Japanese cuisine",
        };
    },
    mounted() {},
    methods: {},
    computed: {},
};
</script>



