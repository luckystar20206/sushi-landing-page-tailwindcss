<template>
    <div class="container mx-auto h-100">
        <img
            :src="currentImage"
            class="transition transition-opacity duration-500 ease-in-out"
        />
    </div>
</template>


<script>
export default {
    name: "Slider",
    components: {},
    data() {
        return {
            index: 0,
            image: "",
            images: [
                "/images/sushi-salmon.jpg",
                "https://i.picsum.photos/id/2/200/300.jpg?hmac=HiDjvfge5yCzj935PIMj1qOf4KtvrfqWX3j4z1huDaU",
                "https://i.picsum.photos/id/3/200/300.jpg?hmac=o1-38H2y96Nm7qbRf8Aua54lF97OFQSHR41ATNErqFc",
            ],
        };
    },
    mounted() {
        this.changeSlide();
    },
    methods: {
        nexSlide() {
            if (this.index === this.images.length - 1) {
                this.index = 0;
            } else {
                this.index++;
            }
        },
        changeSlide() {
            setInterval(() => {
                this.nexSlide();
            }, 2000);
        },
    },
    computed: {
        currentImage() {
            return this.images[this.index];
        },
    },
};
</script>

