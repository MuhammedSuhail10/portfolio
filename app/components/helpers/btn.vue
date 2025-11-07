<script setup lang="ts">
defineProps<{
    text: string;
}>();
</script>

<template>
    <div
        class="cursor-pointer hover:scale-105 hover:border-[#34A0A4] hover:text-[#34A0A4] md:text-[15pt] text-[13pt] md:w-[8em] w-[6em] md:h-[9em] h-[7em] bg-[#181818] flex flex-col items-center justify-center gap-[0.5em] py-[1.5em] rounded-[0.5em] md:rounded-[1em] border-[#F0F8FF] border-[1px]">
        <slot name="icon"></slot>
        <div class='md:text-[1.2em] text-[1em] '>{{ text }}</div>
    </div>
</template>