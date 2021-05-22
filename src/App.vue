<template>
    <main class="flex flex-col h-screen">
        <nav-bar></nav-bar>
        <div class="bg-red-900 text-center py-4">
            <div
                class="p-2 bg-red-700 items-center text-red-100 leading-none lg:rounded-full flex lg:inline-flex"
                role="alert"
            >
                <span
                    class="flex rounded-full bg-red-500 uppercase px-2 py-1 text-xs font-bold mr-3"
                    >News</span
                >
                <span class="font-semibold mr-2 text-left flex-auto"
                    >This page is work in progress</span
                >
            </div>
        </div>

        <div class="flex-1 overflow-y-auto">
            <router-view v-slot="{ Component }">
                <transition name="slide-fade">
                    <component :is="Component" />
                </transition>
            </router-view>
        </div>
    </main>
</template>


<script>
import { defineComponent } from "vue";
import NavBar from "@/components/NavBar.vue";

export default defineComponent({
    components: {
        NavBar,
    },
});
</script>

<style>
.slide-fade-enter-active {
    transition: all 0.3s ease-out;
}

.slide-fade-leave-active {
    transition: all 0.8s cubic-bezier(1, 0.5, 0.8, 1);
}

.slide-fade-enter-from,
.slide-fade-leave-to {
    opacity: 0;
}
</style>
