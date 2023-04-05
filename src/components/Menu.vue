<template>
    <div class="absolute bg-[#333333] py-7 px-5 h-full flex justify-end text-center w-full -translate-x-[calc(100%-120px)] transition-all duration-500 z-50" ref="menu">
        <div class="flex flex-col items-center justify-between">
            <button type="button" @click="toggleMenu">
                <div class="relative w-20">
                    <img src="../assets/images/header/logo.png" alt="" class="absolute transition-all duration-500" ref="logo">
                    <img src="../assets/images/header/logo2.png" alt="" class="absolute transition-all duration-500 opacity-0" ref="logo2">
                </div>
            </button>
            <div class="flex flex-col gap-14 items-center text-white font-bold text-2xl md:text-3xl lg:text-4xl hidden" ref="nav">
                <a href="">Меню</a>
                <a href="">Доставка</a>
                <a href="">Оплата</a>
                <button class="text-2xl px-10 py-5 bg-[#B59571]">Бронь столика</button>
            </div>
            <div class="flex flex-col items-center gap-5">
                <a href="" @click="toggleMenu"><img src="../assets/images/header/youtube.svg" alt=""></a>
                <a href="" @click="toggleMenu"><img src="../assets/images/header/vk.svg" alt=""></a>
                <a href="" @click="toggleMenu"><img src="../assets/images/header/tg.svg" alt=""></a>
            </div>
        </div>
    </div>
</template>

<script>
import { ref } from 'vue';
export default {
    setup() {
        const menu = ref(null);
        const nav = ref(null);
        const logo = ref(null);
        const logo2 = ref(null);
        const toggleMenu = () => {
            menu.value.classList.toggle("-translate-x-[calc(100%-120px)]");
            menu.value.classList.toggle("justify-center");
            nav.value.classList.toggle("hidden");
            logo.value.classList.toggle("opacity-0");
            logo2.value.classList.toggle("opacity-0");
        }
        return { menu, nav, logo, logo2, toggleMenu}
    }
}
</script>

<style>

</style>