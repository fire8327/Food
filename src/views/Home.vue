<template>
    <header class="bg-[url('../src/assets/images/header/background.png')] h-screen w-full relative bg-center flex justify-end md:justify-center items-center">  
        <Menu/>      
        <p class="text-white font-bold max-[375px]:text-2xl text-3xl sm:text-4xl md:text-5xl lg:text-6xl w-[calc(100%-150px)] pr-8 md:px-0 md:w-1/2 2xl:w-1/3">
            Видовой ресторан Food Exxe Relo на Крестовском острове
        </p>
    </header>
</template>

<script>
import Menu from "../components/Menu.vue";
export default {
    components: {
        Menu
    }
}
</script>

<style>

</style>