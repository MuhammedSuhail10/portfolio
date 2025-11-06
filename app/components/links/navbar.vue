<script setup>
const route = useRoute()
const isHome = computed(() => route.path === '/')
const isAbout = computed(() => route.path === '/about')
</script>

<template>
    <div class="text-[15pt] flex justify-between items-center" :class="isHome && 'px-[5em] mt-[1em] h-[4em] ', !isHome && 'h-[6em] px-[10em]' , isAbout && 'text-[#1e1e1e] bg-[#F0F8FF]'">
        <NuxtLink class="font-[600] hover:text-[#34A0A4]" active-class="text-[#34A0A4] font-[800]" exact to="/" >
            Muhammed Suhail
        </NuxtLink>
        <div class="flex gap-10">
            <NuxtLink to="/about" active-class="text-[#34A0A4] font-[800]" exact>About</NuxtLink>
            <NuxtLink to="/work" active-class="text-[#34A0A4] font-[800]" exact>Work</NuxtLink>
            <NuxtLink to="/contact" active-class="text-[#34A0A4] font-[800]" exact>Contact</NuxtLink>
        </div>
    </div>
</template>