<template>
    <div>
        <Carousel :autoplay="6000" :wrap-around="true">
            <Slide v-for="(slide, index) in slides" :key="slide">
                <div
                    class="relative h-48 md:h-96 w-full bg-cover bg-no-repeat flex items-center justify-center"
                    :style="{
                        'background-image': slide.bg,
                        'background-position': backgroundPosition,
                    }"
                >
                    <div class="">
                        <div
                            class="text-1xl md:text-4xl bg-black bg-opacity-50 text-white text-center block px-8 py-2 md:py-8 mb-4"
                        >
                            <span class="opacity-100">{{
                                slide.headLine
                            }}</span>
                        </div>
                    </div>
                </div>
            </Slide>
        </Carousel>
    </div>
</template>

<script>
import { defineComponent } from "vue";
import { Carousel, Navigation, Pagination, Slide } from "vue3-carousel";
import "vue3-carousel/dist/carousel.css";

export default defineComponent({
    name: "SliderHome",
    components: {
        Carousel,
        Slide,
        Pagination,
        Navigation,
    },
    data: () => ({
        slides: [
            {
                headLine:
                    "Enjoy fresh fish & drinks. Immerse yourself in true Japanese cuisine",
                bg: "url('/images/bg-home1.jpg",
            },
            {
                headLine:
                    "Seasonal high-quality ingredients and professional service for lasting dining experience",
                bg: "url('/images/bg-home2.jpg",
            },
        ],
        backgroundPosition: "0 0",
        settings: {
            itemsToShow: 1,
            snapAlign: "center",
        },
    }),
    methods: {
        handleSliderButton(url) {
            // Add a custom event listener to the buttons in slider due to vue3-carousel uses event.preventDefault(); which prevents buttons from working on mobile
            if (!url) {
                return;
            }
            location.href = url;
        },
    },
    mounted() {},
    computed: {},
});
</script>

<style scoped>
</style>