<template>
    <div class="container mx-auto">
        <div
            class="bg-yellow-200 h-auto md:h-96 flex items-center justify-center"
        >
            <div
                class="w-full mx-auto rounded-lg bg-white shadow-lg px-5 pt-5 pb-10 text-gray-800"
                style="max-width: 600px"
            >
                <div class="w-full pt-1 pb-5">
                    <div
                        class="overflow-hidden rounded-full w-20 h-20 mt-0 md:-mt-16 mx-auto shadow-lg"
                    >
                        <img :src="reviewProfile" alt="" />
                    </div>
                </div>
                <div class="w-full mb-10">
                    <div
                        class="text-3xl text-gray-500 text-left leading-tight h-3"
                    >
                        “
                    </div>
                    <p class="text-md text-gray-600 px-5 h-auto md:h-36">
                        {{ review.comment }}
                    </p>
                    <div
                        class="text-3xl text-gray-500 text-right leading-tight h-3 -mt-3"
                    >
                        ”
                    </div>
                </div>
                <div class="w-full">
                    <p class="text-md text-red-500 text-center">
                        {{ review.name }}
                    </p>
                </div>
            </div>
        </div>
    </div>
</template>


<script>
export default {
    name: "SliderReviews",
    components: {},
    data() {
        return {
            index: 0,
            reviews: [
                {
                    comment:
                        "Their food is very high-quality, delicious, and authentic Japanese. It reminds me of the food I ate in Japanese Ryokan which is special.Also, they have many kinds of alcohol which are Japanese sake, shochu, and domestic beer.The decor and atmosphere are great. I spent a great time while I eat there. I highly recommend this place.",
                    name: "Mary Robinson",
                },
                {
                    comment:
                        "We did their take-out Omakase and it was an absolute delight - it's the most fun meal that we've had throughout all of COVID.The sushi is beautifully packaged, and they even give you two cocktails in pretty little glass bottles. They've set up a special website where Chef Phillip Frankland Lee introduces each dish via video, so we were able to get some of that true Omakase experience even though we were at home. ",
                    name: "Natasha Smith",
                },
                {
                    comment:
                        "This place is amazing.  The chef's special squid is very tasty and tender. Service is good.  The deluxe sashimi platter is the best I've had.  The Yellowtail was so fresh and tasty. The x-ray roll is amazing and good for the low carb diet. I highly recommend this place.  Be sure to get in line on Yelp to save time as this place can get busy.",
                    name: "Ann Ryker",
                },
            ],
        };
    },
    mounted() {
        this.changeSlide();
    },
    methods: {
        nexSlide() {
            if (this.index === this.reviews.length - 1) {
                this.index = 0;
            } else {
                this.index++;
            }
        },
        changeSlide() {
            setInterval(() => {
                this.nexSlide();
            }, 6000);
        },
    },
    computed: {
        review() {
            return this.reviews[this.index];
        },
        reviewProfile() {
            return `https://randomuser.me/api/portraits/women/${this.index}.jpg`;
        },
    },
};
</script>

