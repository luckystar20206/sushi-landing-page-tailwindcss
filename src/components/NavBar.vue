
<template>
    <div class="flex flex-wrap">
        <div class="w-full px-4">
            <nav
                class="relative flex flex-wrap items-center justify-between py-2"
            >
                <div
                    class="container mx-auto flex flex-wrap items-center justify-between"
                >
                    <div class="flex justify-between md:w-auto">
                        <a
                            class="text-3xl md:text-5xl py-0 md:py-3 font-bold leading-relaxed inline-block whitespace-nowrap uppercase"
                            href="/"
                        >
                            寿司<span class="text-red-500">SUSHI</span>
                        </a>
                    </div>
                    <span
                        id="hamburgerbtn"
                        class="absolute right-0 top-6 md:hidden"
                    >
                        <svg viewBox="0 0 100 80" width="20" height="20">
                            <rect width="100" height="10"></rect>
                            <rect y="30" width="100" height="10"></rect>
                            <rect y="60" width="100" height="10"></rect>
                        </svg>
                    </span>

                    <div class="flex w-full md:w-auto">
                        <ul
                            id="mainMenu"
                            class="flex flex-col md:flex w-full hidden lg:flex-row list-none ml-auto"
                        >
                            <li class="nav-item">
                                <a
                                    class="px-3 py-2 flex items-center text-xs uppercase font-bold leading-snug hover:opacity-75"
                                    href="menu"
                                >
                                    Menu
                                </a>
                            </li>
                            <!-- <li class="nav-item">
                                <a
                                    class="px-3 py-2 flex items-center text-xs uppercase font-bold leading-snug hover:opacity-75"
                                    href="#"
                                >
                                    About us
                                </a>
                            </li>
                            <li class="nav-item">
                                <a
                                    class="px-3 py-2 flex items-center text-xs uppercase font-bold leading-snug hover:opacity-75"
                                    href="#"
                                >
                                    Contact
                                </a>
                            </li> -->
                        </ul>
                    </div>
                </div>
            </nav>
        </div>
    </div>
</template>


<script>
export default {
    name: "NavBar",
    components: {},
    data() {
        return {};
    },
    mounted() {
        this.initMenu();
    },
    methods: {
        initMenu() {
            let hamburger = document.getElementById("hamburgerbtn");
            let mainMenu = document.getElementById("mainMenu");
            hamburger.addEventListener("click", function () {
                mainMenu.classList.toggle("active");
            });
        },
    },
    computed: {},
};
</script>


<style>
.active {
    display: block;
}
</style>
