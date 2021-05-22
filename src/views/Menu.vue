<template>
    <main>
        <div class="bg-gray-50">
            <div class="relative h-96 mb-12">
                <div
                    class="absolute bg-cover bg-no-repeat inset-0 flex items-center justify-center"
                    style="
                        background-image: url('/images/bg-menu.jpg');
                        background-position: 0 -200px;
                    "
                >
                    <div
                        class="bg-black bg-opacity-50 text-white text-center block px-8 py-2 md:py-8"
                    >
                        <span
                            class="text-1xl sm:text-4xl opacity-100 mb-6 block"
                            >Explore our menu</span
                        >
                        <span
                            class="text-1xl sm:text-1xl text-center text-gray-100 block mb-16"
                        >
                            Originating in Japan, consisting of cooked vinegared
                            rice combined with other ingredients such as raw
                            seafood and vegetables
                        </span>
                    </div>
                </div>
            </div>

            <h2
                class="text-3xl text-center uppercase block mb-6"
                id="menu-sushi"
            >
                Sushi menu
            </h2>
            <h3 class="text-1xl text-center text-gray-700 block mb-16">
                Our fish are always fresh and every dish is made to order.
            </h3>
            <menu-sushi></menu-sushi>

            <h2
                class="text-3xl text-center uppercase block mb-6"
                id="menu-kitchen"
            >
                Kitchen menu
            </h2>
            <h3 class="text-1xl text-center text-gray-700 block mb-16">
                From salad to yakitori and noodles, your friends and family are
                bound to find something to enjoy
            </h3>
            <menu-kitchen></menu-kitchen>
            <h2
                class="text-3xl text-center uppercase block mb-6"
                id="menu-drinks"
            >
                Drinks menu
            </h2>
            <h3 class="text-1xl text-center text-gray-700 block mb-16">
                Unwind with our wide selection of beers, Japanese sake, shochu
                and refreshing whisky highballs shochu
            </h3>
            <menu-drinks></menu-drinks>
        </div>
    </main>
</template>


<script>
import MenuSushi from "@/components/MenuSushi.vue";
import MenuKitchen from "@/components/MenuKitchen.vue";
import MenuDrinks from "@/components/MenuDrinks.vue";

export default {
    name: "Home",
    components: {
        MenuSushi,
        MenuKitchen,
        MenuDrinks,
    },
    data() {
        return {};
    },
    mounted() {},
    methods: {},
    computed: {},
};
</script>
