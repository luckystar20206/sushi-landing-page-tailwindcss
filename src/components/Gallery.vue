
<template>
    <div class="container mx-auto">
        <section class="py-4 px-4">
            <div class="flex flex-wrap -mx-4">
                <div class="hidden md:block md:w-1/2 px-4">
                    <div
                        class="h-full w-full bg-cover rounded shadow-md"
                        style="
                            background-image: url('/images/gallery-images-3.jpg');
                        "
                    ></div>
                </div>
                <div class="md:w-1/2 h-auto px-4">
                    <div class="mb-8">
                        <img
                            class="rounded shadow-md"
                            src="/images/gallery-images-2.jpg"
                            alt=""
                        />
                    </div>
                    <div>
                        <img
                            class="rounded shadow-md"
                            src="/images/gallery-images-1.jpg"
                            alt=""
                        />
                    </div>
                </div>
            </div>
        </section>

        <section class="pt-8 px-4">
            <div class="flex flex-wrap -mx-4">
                <div class="md:w-1/3 px-4 mb-8">
                    <img
                        class="rounded shadow-md"
                        src="/images/gallery-images-4.jpg"
                        alt=""
                    />
                </div>
                <div class="md:w-1/3 px-4 mb-8">
                    <img
                        class="rounded shadow-md"
                        src="/images/gallery-images-5.jpg"
                        alt=""
                    />
                </div>
                <div class="md:w-1/3 px-4 mb-8">
                    <img
                        class="rounded shadow-md"
                        src="/images/gallery-images-6.jpg"
                        alt=""
                    />
                </div>
            </div>
        </section>
    </div>
</template>


<script>
export default {
    name: "Gallery",
    components: {},
    data() {
        return {};
    },
    mounted() {},
    methods: {},
    computed: {},
};
</script>











