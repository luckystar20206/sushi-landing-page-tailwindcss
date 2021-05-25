<template>
    <main>
        <div class="bg-gray-50">
            <slider-home></slider-home>
            <cta></cta>

            <h2 class="text-2xl md:text-4xl text-center uppercase block mb-6">
                Explore our menu
            </h2>
            <h3 class="text-1xl text-center text-gray-700 block mb-16">
                Originating in Japan, consisting of cooked vinegared rice
                combined with other ingredients such as raw seafood and
                vegetables
            </h3>

            <category-cards></category-cards>

            <div class="mb-16"></div>

            <home-parallax></home-parallax>

            <div class="mb-16"></div>

            <div
                class="container mx-auto grid grid-cols-1 md:grid-cols-2 gap-4 place-items-center"
            >
                <div class="w-full">
                    <h2
                        class="text-2xl md:text-4xl text-center uppercase block mb-6"
                    >
                        Hours
                    </h2>

                    <operation-hours></operation-hours>
                </div>

                <div class="w-full">
                    <h2
                        class="text-2xl md:text-4xl text-center uppercase block mb-6"
                    >
                        Location
                    </h2>
                    <location></location>
                </div>
            </div>
        </div>
        <div class="mb-16"></div>

        <h2 class="text-2xl md:text-4xl text-center uppercase block mb-6">
            Customer reviews
        </h2>

        <slider-reviews></slider-reviews>

        <div class="mb-16"></div>

        <h2 class="text-2xl md:text-4xl text-center uppercase block mb-6">
            Gallery
        </h2>

        <gallery></gallery>
    </main>
</template>


<script>
import HomeBackground from "@/components/HomeBackground.vue";
import CategoryCards from "@/components/CategoryCards.vue";
import HomeParallax from "@/components/HomeParallax.vue";
import OperationHours from "@/components/OperationHours.vue";
import Location from "@/components/Location.vue";
import SliderReviews from "@/components/SliderReviews.vue";
import Gallery from "@/components/Gallery.vue";
import SliderHome from "@/components/SliderHome.vue";
import Cta from "@/components/Cta.vue";

export default {
    name: "Home",
    components: {
        HomeBackground,
        CategoryCards,
        HomeParallax,
        OperationHours,
        Location,
        SliderReviews,
        Gallery,
        SliderHome,
        Cta,
    },
    data() {
        return {};
    },
    mounted() {},
    methods: {},
    computed: {},
};
</script>
