<script setup>
const route = useRoute()
const isHome = computed(() => route.path === '/')
</script>

<template>
    <div class="font-[outfit] bg-[#0f0f0f] text-[#F0F8FF]">
        <div :class="isHome && 'hidden'">
            <LinksNavbar />
        </div>
        <NuxtPage />
        <LinksFooter />
    </div>
</template>