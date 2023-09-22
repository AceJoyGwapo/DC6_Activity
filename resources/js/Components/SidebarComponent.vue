<script setup>
import LinkSection from '@/Components/LinkSection.vue';
import { Link } from '@inertiajs/vue3';

defineProps({
    isCollapsed: Boolean
})
</script>

<template>
    <nav>
        <Link href="/dashboard" class="flex items-center space-x-2">
            <img src="https://static.vecteezy.com/system/resources/thumbnails/009/613/452/small/ace-triangle-letter-logo-design-with-triangle-shape-ace-triangle-logo-design-monogram-ace-triangle-logo-template-with-red-color-ace-triangular-logo-simple-elegant-and-luxurious-logo-vector.jpg" alt="" class="w-[30px] rounded-sm">
            <span v-show="!isCollapsed" class="text-2xl text-white font-extrabold">AceJoy Villarmia</span>
        </Link>
        <hr class="mt-4">

        <span v-show="!isCollapsed" class="text-[10px] uppercase font-bold text-gray-300 select-none">Navigation</span>

        <LinkSection :isCollapsed="isCollapsed" />
    </nav>
</template>