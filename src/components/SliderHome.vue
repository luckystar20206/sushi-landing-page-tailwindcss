<template>
    <div>
        <Carousel :autoplay="6000" :wrap-around="true" class="mb-0 md:mb-12">
            <Slide
                v-for="(slide, index) in slides"
                :key="slide"
                class="relative h-screen"
            >
                <div
                    class="absolute bg-cover bg-no-repeat inset-0 flex items-center justify-center"
                    :style="{
                        'background-image': slide.bg,
                        'background-position': backgroundPosition,
                    }"
                >
                    <div class="">
                        <div
                            class="text-1xl md:text-4xl bg-black bg-opacity-50 text-white text-center block px-8 py-2 -mt-16 md:py-8"
                        >
                            <span class="opacity-100">{{
                                slide.headLine
                            }}</span>
                        </div>
                        <div
                            class="h-32 flex flex-wrap content-around justify-center gap-2 md:gap-4"
                        >
                            <button
                                class="text-xs md:text-base bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-2 rounded"
                            >
                                Make a reservation
                            </button>
                            <button
                                class="text-xs md:text-base bg-white hover:bg-gray-200 text-gray-700 font-bold py-2 px-2 rounded"
                            >
                                <a href="menu">View Menu</a>
                            </button>
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
        backgroundPosition: "0 -200px",
        settings: {
            itemsToShow: 1,
            snapAlign: "center",
        },
    }),
    computed: {},
});
</script>

<style scoped>
/* Temporary fix for not being able to scroll down on mobile using vu3-carousel. Trying to scroll down triggers sliding to next slider instead. */
/* @media screen and (max-width: 640px) {
    .carousel {
        pointer-events: none;
    }
} */
</style>