<script setup lang='ts'>
defineProps<{
    title: string;
    desc: string;
    year?: string;
    showYear?: boolean;
}>();
</script>

<template>
    <div class='flex justify-between items-center cursor-default '>
        <h1 class=' pt-[0.5em] font-[Outfit] lg:text-[38pt] text-[2em]'><strong>{{title}}</strong></h1>
        <h1 v-if="showYear" class='font-[Outfit] md:pt-[2em] pt-[1em] md:text-[1.1em] text-[0.8em] '>{{year}}</h1>
    </div>
    <h1 class='font-[Outfit] cursor-default md:text-[15pt] italic text-[1em] text-[#bed3e7] '>{{desc}}</h1>
    <hr class='opacity-25 mt-[1em]' />
</template>