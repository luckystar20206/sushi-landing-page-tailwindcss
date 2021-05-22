
<template>
    <div class="relative h-96 mb-16">
        <div
            class="absolute bg-cover bg-fixed bg-no-repeat inset-0 flex items-center justify-center"
            style="background-image: url('/images/bg-sushichef.jpg')"
        >
            <div
                class="container mx-auto grid grid-cols-1 md:grid-cols-2 gap-4"
            >
                <div></div>
                <div
                    class="rounded overflow-hidden flex flex-wrap justify-center"
                >
                    <h4 class="text-2xl md:text-4xl text-white mb-12">
                        {{ headline }}
                    </h4>
                    <p
                        class="bg-black bg-opacity-50 px-4 py-4 md:px-8 py-8 text-white"
                    >
                        <span class="block mb-8"
                            >We specialize in traditional authentic sushi and
                            other popular Japanese cuisine. Let our experienced
                            sushi chefs, all with over a decade of experience
                            provide you with fresh fish and an true Japanese
                            culinary experience.
                        </span>
                        <span class="block text-right text-gray-400"
                            >Mike Takahashi - Owner</span
                        >
                    </p>
                </div>
            </div>
        </div>
    </div>
</template>


<script>
export default {
    name: "HomeParallax",
    components: {},
    data() {
        return {
            headline: "About us",
        };
    },
    mounted() {},
    methods: {},
    computed: {},
};
</script>



